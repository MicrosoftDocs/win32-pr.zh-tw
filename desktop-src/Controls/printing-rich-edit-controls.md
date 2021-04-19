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
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="207b5-103">如何列印 Rich Edit 控制項的內容</span><span class="sxs-lookup"><span data-stu-id="207b5-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="207b5-104">本章節包含如何列印 rich edit 控制項內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="207b5-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="207b5-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="207b5-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="207b5-106">技術</span><span class="sxs-lookup"><span data-stu-id="207b5-106">Technologies</span></span>

-   [<span data-ttu-id="207b5-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="207b5-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="207b5-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="207b5-108">Prerequisites</span></span>

-   <span data-ttu-id="207b5-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="207b5-109">C/C++</span></span>
-   <span data-ttu-id="207b5-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="207b5-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="207b5-111">指示</span><span class="sxs-lookup"><span data-stu-id="207b5-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="207b5-112">使用預覽列印</span><span class="sxs-lookup"><span data-stu-id="207b5-112">Use Print Preview</span></span>

<span data-ttu-id="207b5-113">若要格式化 rich edit 控制項中的文字，因為它會顯示在目標裝置上 (通常是列印的頁面) ，傳送 [**EM \_ SETTARGETDEVICE**](em-settargetdevice.md) 訊息，並將控制碼傳遞至裝置內容 (依目標裝置的 HDC) 以及所需的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="207b5-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="207b5-114">通常您會藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) 來取得目標 HDC 的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="207b5-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="207b5-115">特定裝置的格式列印</span><span class="sxs-lookup"><span data-stu-id="207b5-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="207b5-116">若要為特定裝置格式化豐富編輯控制項內容的一部分，請傳送 [**EM \_ FORMATRANGE**](em-formatrange.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="207b5-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="207b5-117">與此訊息搭配使用的 [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) 結構會指定要格式化的文字範圍，以及目標裝置的 HDC。</span><span class="sxs-lookup"><span data-stu-id="207b5-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="207b5-118">（選擇性）此訊息也會將文字傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="207b5-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="207b5-119">使用條紋</span><span class="sxs-lookup"><span data-stu-id="207b5-119">Use Banding</span></span>

<span data-ttu-id="207b5-120">「群組」是使用一或多個不同的矩形或群組來產生單一輸出頁面的處理常式。</span><span class="sxs-lookup"><span data-stu-id="207b5-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="207b5-121">當所有條紋都放在頁面上時，就會產生完整的影像結果。</span><span class="sxs-lookup"><span data-stu-id="207b5-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="207b5-122">這種方法通常是由沒有足夠記憶體的點陣印表機，或一次影像一整頁的功能所使用。</span><span class="sxs-lookup"><span data-stu-id="207b5-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="207b5-123">若要執行分級，請使用 [**EM \_ DISPLAYBAND**](em-displayband.md) 訊息，將 rich edit 控制項內容的後續部分傳送到裝置。</span><span class="sxs-lookup"><span data-stu-id="207b5-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="207b5-124">這則訊息會列印到在先前的 [**EM \_ FORMATRANGE**](em-formatrange.md)呼叫中所指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="207b5-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="207b5-125">當然， **EM \_ FORMATRANGE** 訊息的 *wParam* 參數應為零，如此一來，就不會由該訊息起始列印。</span><span class="sxs-lookup"><span data-stu-id="207b5-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="207b5-126">PrintRTF 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="207b5-126">PrintRTF Code Example</span></span>

<span data-ttu-id="207b5-127">下列程式碼範例會將 rich edit 控制項的內容列印到指定的印表機。</span><span class="sxs-lookup"><span data-stu-id="207b5-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="207b5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="207b5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="207b5-129">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="207b5-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="207b5-130">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="207b5-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 