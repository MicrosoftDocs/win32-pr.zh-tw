---
title: 從您的延伸模組取得 ADSI 介面
description: 延伸模組通常需要從它所系結的目錄物件取得資料。
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- 擴充功能 ADSI，從您的延伸模組取得 ADSI 介面
- ADSI ADSI，範例程式碼 C/c + +，從您的延伸模組取得 ADSI 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106984945"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>從您的延伸模組取得 ADSI 介面

延伸模組通常需要從它所系結的目錄物件取得資料。 例如， **電腦** 物件的延伸模組可能會想要從目錄取得目前物件的 **dnsHostName** 。 您可以在匯總工具的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面上發出 **QueryInterface** 呼叫，輕鬆達成這個目的。


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



您應該在使用介面之後立即加以釋放。 如果延伸模組具有匯總工具的開啟參考，則您已建立迴圈參考，且匯總工具無法釋放延伸模組。 因此，無法釋放匯總工具，且結果會在您的應用程式中造成記憶體流失。

 

 