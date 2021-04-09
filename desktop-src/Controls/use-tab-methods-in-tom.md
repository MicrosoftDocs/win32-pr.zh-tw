---
title: 如何在 TOM 中使用 Tab 方法
description: 下列範例提供的 C 函式說明如何使用 Text 物件模型中的 tab 方法 (TOM) 。
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841996"
---
# <a name="how-to-use-tab-methods-in-tom"></a>如何在 TOM 中使用 Tab 方法

下列範例提供的 C 函式說明如何使用 Text 物件模型中的 tab 方法 (TOM) 。 假設大部分的應用程式都包含工具列，以顯示目前所選取段落的目前位置和索引標籤類型。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-tab-method"></a>使用 Tab 方法

下列程式碼範例示範如何使用目前的索引標籤詳細資料來更新工具列。


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a>複製索引標籤資訊

下列範例顯示如何只將索引標籤資訊從一個 [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) 介面複製到另一個介面。 它會採用兩個參數： **ITextPara** \* *pParaFrom* (要複製索引標籤的段落) 和 **ITextPara** \* *pParaFrom* () 複製索引標籤的段落。


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Text 物件模型](using-the-text-object-model.md)
</dt> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




