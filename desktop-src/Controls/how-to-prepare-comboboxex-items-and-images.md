---
title: 如何準備 ComboBoxEx 專案和影像
description: 本主題將示範如何將專案加入至 ComboBoxEx 控制項。
ms.assetid: 2603DFBE-9E7A-4B2F-BE33-418997D323B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7474b46e5227d91b1cc2b51462a43a0fb75d8b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842759"
---
# <a name="how-to-prepare-comboboxex-items-and-images"></a>如何準備 ComboBoxEx 專案和影像

本主題將示範如何將專案加入至 ComboBoxEx 控制項。

若要將專案加入至 ComboBoxEx 控制項，請先定義 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構。 然後，設定結構的 **遮罩** 成員，以指出您希望控制項使用哪些成員。 最後，將結構的指定成員設定為所需的值，然後傳送 [**CBEM \_ INSERTITEM**](cbem-insertitem.md) 訊息，將專案加入至控制項。

下列應用程式定義函數會將15個專案加入至現有的 ComboBoxEx 控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

若要將專案加入至 ComboBoxEx 控制項，請先定義 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構。


```C++
COMBOBOXEXITEM cbei;
int iCnt;


typedef struct {
    int iImage;
    int iSelectedImage;
    int iIndent;
    LPTSTR pszText;
} ITEMINFO, *PITEMINFO;

ITEMINFO IInf[ ] = {
    { 0, 3,  0, L"first"}, 
    { 1, 4,  1, L"second"},
    { 2, 5,  2, L"third"},
    { 0, 3,  0, L"fourth"},
    { 1, 4,  1, L"fifth"},
    { 2, 5,  2, L"sixth"},
    { 0, 3,  0, L"seventh"},
    { 1, 4,  1, L"eighth"},
    { 2, 5,  2, L"ninth"},
    { 0, 3,  0, L"tenth"},
    { 1, 4,  1, L"eleventh"},
    { 2, 5,  2, L"twelfth"},
    { 0, 3,  0, L"thirteenth"},
    { 1, 4,  1, L"fourteenth"},
    { 2, 5,  2, L"fifteenth"}
};
```



### <a name="step-2"></a>步驟 2:

設定結構的 **遮罩** 成員，以指出您希望控制項使用哪些成員。 請注意， [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **mask** 成員包含旗標值，這些值會告訴控制項顯示每個專案的影像。


```C++
// Set the mask common to all items.
cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
            CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;
```



### <a name="step-3"></a>步驟 3：

將結構的指定成員設為您想要的值，然後傳送 [**CBEM \_ INSERTITEM**](cbem-insertitem.md) 訊息，將專案加入至控制項。


```C++
for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
    // Initialize the COMBOBOXEXITEM struct.
    cbei.iItem          = iCnt;
    cbei.pszText        = IInf[iCnt].pszText;
    cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
    cbei.iImage         = IInf[iCnt].iImage;
    cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
    cbei.iIndent        = IInf[iCnt].iIndent;

    
    // Tell the ComboBoxEx to add the item. Return FALSE if 
    // this fails.
    if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
        return FALSE;
```



### <a name="step-4"></a>步驟 4：

將現有的影像清單指派給 ComboBoxEx 控制項，並設定控制項的大小。


```C++
// Assign the existing image list to the ComboBoxEx control 
// and return TRUE. 
// g_himl is the handle to the existing image list
SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

// Set size of control to make sure it's displayed correctly now
// that the image list is set.
SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

return TRUE; 
```



## <a name="complete-example"></a>完整範例


```C++
// AddItems - Uses the CBEM_INSERTITEM message to add items to an
// existing ComboBoxEx control.

BOOL WINAPI AddItems(HWND hwndCB)
{
    
    //  Declare and init locals.
    COMBOBOXEXITEM cbei;
    int iCnt;
    

    typedef struct {
        int iImage;
        int iSelectedImage;
        int iIndent;
        LPTSTR pszText;
    } ITEMINFO, *PITEMINFO;

    ITEMINFO IInf[ ] = {
        { 0, 3,  0, L"first"}, 
        { 1, 4,  1, L"second"},
        { 2, 5,  2, L"third"},
        { 0, 3,  0, L"fourth"},
        { 1, 4,  1, L"fifth"},
        { 2, 5,  2, L"sixth"},
        { 0, 3,  0, L"seventh"},
        { 1, 4,  1, L"eighth"},
        { 2, 5,  2, L"ninth"},
        { 0, 3,  0, L"tenth"},
        { 1, 4,  1, L"eleventh"},
        { 2, 5,  2, L"twelfth"},
        { 0, 3,  0, L"thirteenth"},
        { 1, 4,  1, L"fourteenth"},
        { 2, 5,  2, L"fifteenth"}
    };

    // Set the mask common to all items.
    cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
                CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;

    for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
        // Initialize the COMBOBOXEXITEM struct.
        cbei.iItem          = iCnt;
        cbei.pszText        = IInf[iCnt].pszText;
        cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
        cbei.iImage         = IInf[iCnt].iImage;
        cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
        cbei.iIndent        = IInf[iCnt].iIndent;
    
        
        // Tell the ComboBoxEx to add the item. Return FALSE if 
        // this fails.
        if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
            return FALSE;
    }
    // Assign the existing image list to the ComboBoxEx control 
    // and return TRUE. 
    // g_himl is the handle to the existing image list
    SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

    // Set size of control to make sure it's displayed correctly now
    // that the image list is set.
    SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

    return TRUE; 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 ComboBoxEx 控制項](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx 控制項參考](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[使用 ComboBoxEx 控制項](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 