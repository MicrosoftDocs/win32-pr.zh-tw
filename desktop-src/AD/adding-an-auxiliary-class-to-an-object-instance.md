---
title: 將輔助類別加入至物件實例
description: 下列程式碼範例示範如何使用 ADSI 和 LDAP，將輔助類別動態新增至現有的物件實例。
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023296"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>將輔助類別加入至物件實例

下列程式碼範例示範如何使用 ADSI 和 LDAP，將輔助類別動態新增至現有的物件實例。 這些範例假設名為 **車輛** 的輔助類別是在 Active Directory 架構中定義，而且 **車輛** 類別具有 **vin** 屬性。

當您將輔助類別動態加入至物件實例時，您必須同時為類別中的任何強制 **mustHave** 屬性指定值。 下列範例示範如何使用 "vin" 屬性來執行此動作，這會假設為強制性。

下列 c + + 範例會系結至物件，並使用 [**IADs PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) 將輔助類別附加至物件的 **objectClass** 屬性中的類別清單。 然後，此範例會使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-put) 來設定 **vin** 屬性的值。 最後，它會呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可目錄的變更。


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 