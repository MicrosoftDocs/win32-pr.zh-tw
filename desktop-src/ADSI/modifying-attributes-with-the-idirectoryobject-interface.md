---
title: 使用 IDirectoryObject 介面修改屬性
description: 除了 IADs Put 和 IADs PutEx 之外，您還可以使用 IDirectoryObject SetObjectAttributes 方法來修改屬性值。 若要使用這個方法，您必須 \_ \_ 為每個要修改的屬性填入 ADS ATTR 資訊結構。
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- 使用 IDirectoryObject 介面 ADSI 修改屬性
- IDirectoryObject ADSI，用來修改屬性
- ADSI ADSI，範例程式碼 C/c + +，使用 IDirectoryObject 修改屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179026"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>使用 IDirectoryObject 介面修改屬性

除了 [**IADs：:P**](/windows/desktop/api/Iads/nf-iads-iads-put) 的 [**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex)，您也可以使用 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) 方法來修改屬性值。 若要使用這個方法，您必須為每個要修改的屬性填入 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) 結構。

[**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)方法可讓您修改單一值和多重值屬性。 這個函式會提供類似的操作控制項，例如清除、附加、刪除及更新，以及 [**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法中找到的控制項。 控制項常數包括：

-   [**ADS \_ ATTR \_ CLEAR**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ 更新**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ 附加**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ 刪除**](adsi-attribute-modification-types.md)

指定 [**ADS \_ ATTR \_ UPDATE**](adsi-attribute-modification-types.md) 將會觸發可能耗用大量資源的伺服器端作業。 例如，初始化作業以更新群組成員資格的長清單。 一般而言，除非修改牽涉到目錄中的少數屬性，否則請避免使用這項操作。 若要修改較長的群組成員資格清單，更有效率的方法是從基礎目錄讀取清單、進行修改，然後將更新的清單儲存回目錄。

> [!Note]  
> 如同 [**IADs：:P**](/windows/desktop/api/Iads/nf-iads-iads-put) 的 [**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) With [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)，屬性變更可能會在 Active Directory 中完整認可或捨棄。 如果不允許有一或多項修改，因而無法執行，則對屬性進行的任何集體修改都不會認可至該目錄。

 

## <a name="example"></a>範例

下列程式碼範例示範如何使用 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) 方法修改單一和多重值屬性。


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




