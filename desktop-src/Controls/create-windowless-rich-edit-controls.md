---
title: 如何提供視窗功能的無視窗 Rich Edit 控制項
description: 視窗功能包括接收訊息的能力，以及要在其中繪製之裝置內容的擁有權。 無視窗的 rich edit 控制項可透過一對介面 ITextServices 和 ITextHost 來接收這項功能。
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103933025"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>如何提供視窗功能的無視窗 Rich Edit 控制項

視窗功能包括接收訊息的能力，以及要在其中繪製之裝置內容的擁有權。 無視窗的 rich edit 控制項可透過一對介面接收這項功能： [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 和 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="establish-the-window-functionality"></a>建立視窗功能

下列範例程式碼示範如何建立文字主機和文字服務。


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a>備註

程式碼範例中的 *hmodRichEdit* 參數是 Msftedit.dll 模組的控制碼，並假設已透過呼叫 **GetModuleHandle** 函式來取出此控制碼。

## <a name="complete-example"></a>完整範例

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用無視窗的 Rich Edit 控制項](using-windowless-rich-edit-controls.md)
</dt> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




