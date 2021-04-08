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
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="d46c9-103">將輔助類別加入至物件實例</span><span class="sxs-lookup"><span data-stu-id="d46c9-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="d46c9-104">下列程式碼範例示範如何使用 ADSI 和 LDAP，將輔助類別動態新增至現有的物件實例。</span><span class="sxs-lookup"><span data-stu-id="d46c9-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="d46c9-105">這些範例假設名為 **車輛** 的輔助類別是在 Active Directory 架構中定義，而且 **車輛** 類別具有 **vin** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d46c9-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="d46c9-106">當您將輔助類別動態加入至物件實例時，您必須同時為類別中的任何強制 **mustHave** 屬性指定值。</span><span class="sxs-lookup"><span data-stu-id="d46c9-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="d46c9-107">下列範例示範如何使用 "vin" 屬性來執行此動作，這會假設為強制性。</span><span class="sxs-lookup"><span data-stu-id="d46c9-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="d46c9-108">下列 c + + 範例會系結至物件，並使用 [**IADs PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) 將輔助類別附加至物件的 **objectClass** 屬性中的類別清單。</span><span class="sxs-lookup"><span data-stu-id="d46c9-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="d46c9-109">然後，此範例會使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-put) 來設定 **vin** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d46c9-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="d46c9-110">最後，它會呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可目錄的變更。</span><span class="sxs-lookup"><span data-stu-id="d46c9-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


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



 

 