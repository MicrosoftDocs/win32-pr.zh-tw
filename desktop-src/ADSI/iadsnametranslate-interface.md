---
title: IADsNameTranslate 介面
description: IADsNameTranslate 介面是用來轉譯各種格式之間的分辨名稱。 名稱轉譯是在目錄伺服器上執行，而且這個介面目前僅供 Active Directory 中的物件使用。
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- IADsNameTranslate 介面 ADSI
- 使用 IADsTranslate ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839180"
---
# <a name="iadsnametranslate-interface"></a>IADsNameTranslate 介面

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)介面是用來轉譯各種格式之間的分辨名稱。 名稱轉譯是在目錄伺服器上執行，而且這個介面目前僅供 Active Directory 中的物件使用。

下列程式碼範例會將帳戶名稱從 Windows 格式轉換為 LDAP 格式。


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




