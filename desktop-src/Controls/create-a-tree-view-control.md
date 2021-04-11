---
title: 如何建立 Tree-View 控制項
description: 若要建立樹狀檢視控制項，請使用 CreateWindowEx 函式，指定 \_ window 類別的 WC TREEVIEW 值。
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093391"
---
# <a name="how-to-create-a-tree-view-control"></a>如何建立 Tree-View 控制項

若要建立樹狀檢視控制項，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，指定 window 類別的 [**WC \_ TREEVIEW**](common-control-window-classes.md) 值。 載入通用控制項 DLL 時，會在應用程式的位址空間中註冊樹狀檢視視窗類別。 若要確定已載入 DLL，請使用 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 函數。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-an-instance-of-a-tree-view-control"></a>建立 Tree-View 控制項的實例

下列範例會建立一個樹狀檢視控制項，其大小調整為符合父視窗的工作區。 它也會使用應用程式定義的函式，將影像清單與控制項建立關聯，並將專案加入控制項。


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>備註

當您建立樹狀檢視控制項時，您也可以將 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息傳送給它，以設定要用於文字的字型。 您應該先傳送此訊息，然後再插入任何專案。 根據預設，樹狀檢視會使用圖示標題字型。 雖然您可以使用 [自訂繪製](custom-draw.md)來自訂每個專案的字型，但是樹狀檢視控制項會使用 **WM \_ SETFONT** 訊息所指定的字型維度來判斷間距和配置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Tree-View 控制項](using-treeview.md)
</dt> <dt>

[CustDTv 範例說明 Tree-View 控制項中的自訂繪圖](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 