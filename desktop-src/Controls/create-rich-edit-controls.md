---
title: 如何建立 Rich Edit 控制項
description: 若要建立 rich edit 控制項，請呼叫 CreateWindowEx 函數，並指定 rich edit 視窗類別。
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024144"
---
# <a name="how-to-create-rich-edit-controls"></a>如何建立 Rich Edit 控制項

若要建立 rich edit 控制項，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數，並指定 rich edit 視窗類別。 若為 Microsoft Rich Edit 4.1 (Msftedit.dll) ，請 \_ 將 Msftedit.dll 類別指定為 window 類別。 針對所有先前的版本，請指定 RICHEDIT \_ 類別。 如需詳細資訊，請參閱 [Rich Edit 的版本](about-rich-edit-controls.md)。

Rich edit 控制項支援大部分與編輯控制項搭配使用的視窗樣式，以及額外的樣式。 如果您想要在控制項中允許一個以上的文字，您應該指定 [**ES \_ 多**](edit-control-styles.md) 行的視窗樣式。 如需詳細資訊，請參閱 [Rich Edit 控制項樣式](rich-edit-control-styles.md)。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-a-rich-edit-control"></a>建立 Rich Edit 控制項

下列範例函式會建立 rich edit 控制項，並使用一些文字將它初始化。


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



在 Microsoft Visual Studio 2005 和更新版本中，您可以從 [工具箱] 拖曳控制項，將 rich edit 控制項新增至對話方塊範本。 不過，在對話方塊編輯器中執行此操作，並無法確保在建立控制項之前，將會載入所需的程式庫。 必須先呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來載入 Riched32.dll、Riched20.dll 或 Msftedit.dll，才能建立對話方塊。

## <a name="remarks"></a>備註

若要搭配這些控制項使用視覺化樣式，應用程式必須包含資訊清單，而且必須在程式的開頭呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 函式。 如需視覺化樣式的詳細資訊，請參閱 [視覺化樣式](themes-overview.md)。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 