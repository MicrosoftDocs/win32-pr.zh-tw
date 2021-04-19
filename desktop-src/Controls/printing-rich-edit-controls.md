---
title: 如何列印 Rich Edit 控制項的內容
description: 本章節包含如何列印 rich edit 控制項內容的相關資訊。
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969732"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>如何列印 Rich Edit 控制項的內容

本章節包含如何列印 rich edit 控制項內容的相關資訊。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-print-preview"></a>使用預覽列印

若要格式化 rich edit 控制項中的文字，因為它會顯示在目標裝置上 (通常是列印的頁面) ，傳送 [**EM \_ SETTARGETDEVICE**](em-settargetdevice.md) 訊息，並將控制碼傳遞至裝置內容 (依目標裝置的 HDC) 以及所需的線條寬度。 通常您會藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) 來取得目標 HDC 的線條寬度。

### <a name="format-print-for-a-specific-device"></a>特定裝置的格式列印

若要為特定裝置格式化豐富編輯控制項內容的一部分，請傳送 [**EM \_ FORMATRANGE**](em-formatrange.md) 訊息。 與此訊息搭配使用的 [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) 結構會指定要格式化的文字範圍，以及目標裝置的 HDC。 （選擇性）此訊息也會將文字傳送至印表機。

### <a name="use-banding"></a>使用條紋

「群組」是使用一或多個不同的矩形或群組來產生單一輸出頁面的處理常式。 當所有條紋都放在頁面上時，就會產生完整的影像結果。 這種方法通常是由沒有足夠記憶體的點陣印表機，或一次影像一整頁的功能所使用。

若要執行分級，請使用 [**EM \_ DISPLAYBAND**](em-displayband.md) 訊息，將 rich edit 控制項內容的後續部分傳送到裝置。 這則訊息會列印到在先前的 [**EM \_ FORMATRANGE**](em-formatrange.md)呼叫中所指定的裝置。 當然， **EM \_ FORMATRANGE** 訊息的 *wParam* 參數應為零，如此一來，就不會由該訊息起始列印。

## <a name="printrtf-code-example"></a>PrintRTF 程式碼範例

下列程式碼範例會將 rich edit 控制項的內容列印到指定的印表機。


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 