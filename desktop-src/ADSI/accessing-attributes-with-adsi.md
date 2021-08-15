---
title: 使用 ADSI 存取屬性
description: IADs 和 IADs. GetEx 方法是用來取出指名的屬性值。
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- 使用 ADSI 存取的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e37c63b61986a56e7b22f114b5956d9e047f1ae45b5dc2e653074ea35440f10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024126"
---
# <a name="accessing-attributes-with-adsi"></a>使用 ADSI 存取屬性

[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)和 [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法是用來取出指名的屬性值。 這兩種方法都會傳回 [**變異**](/windows/win32/api/oaidl/ns-oaidl-variant) 值。 這些方法僅適用于支援架構的目錄。 存取沒有架構的目錄中的物件時，必須使用 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) 和 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) 介面來操作屬性值。

[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)和 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-getex)會根據伺服器傳回的值數目，傳回可能（或可能不是）**變數** 陣列的 [**變異**](/windows/win32/api/oaidl/ns-oaidl-variant)。 例如，如果伺服器只傳回一個值，而不論它是單一值或多重值屬性，則方法會傳回單一 **VARIANT**。 相反地，如果傳回多個值，則會傳回 **VARIANT** 陣列。 如果傳回 **variant** 陣列， **variant** 結構的 **vt** 成員會包含 **vt \_ VARIANT/vbVariant** 和 **vt \_ array/vbArray** 旗標。

[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)和 [**IADs 的 GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法也可以使用 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面傳回 COM 物件。 在此情況下， [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)結構的 **vt** 成員會包含 **vt \_ 分派/vbObject** 旗標。 若要存取 COM 物件，請呼叫 **IDispatch** 介面上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得所需的介面。

[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)所傳回的另一個資料類型為二進位 [**資料。**](/windows/desktop/api/Iads/nf-iads-iads-getex) 在此情況下，資料會以連續的位元組陣列形式提供，而 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)結構的 **vt** 成員將包含 **Vt \_ UI1/vbByte** 和 **vt \_ array/vbArray** 旗標。

> [!Note]  
> Microsoft Visual Basic，腳本撰寫版僅支援 [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant)和 **variant** 陣列。 因此，VBScript 無法用來讀取二進位屬性值。

 

許多 ADSI 介面會定義介面特定屬性。 例如， [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) 介面會定義 [**Location**](iadscomputer-property-methods.md) 屬性。 這些介面定義的屬性可能包含與其中一個已命名屬性相同的資料，但這些屬性是由介面所參考的物件類型所特有。 在支援自動化的語言中，您可以使用點標記法來存取這些介面定義的屬性，如下列程式碼範例所示。

## <a name="examples"></a>範例

下列程式碼範例顯示如何存取 IADs 介面上的 ADsPath 屬性。


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



在非自動化語言中，必須使用屬性存取方法來存取介面定義的屬性。 例如， [**IADsComputer：： get \_ Location**](iadscomputer-property-methods.md) 方法是用來取出 **IADsComputer. location** 屬性。

下列 c + + 程式碼範例示範如何在 c + + 中使用屬性存取方法，以取得使用者的 ADsPath。


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



如需使用 ADSI 存取屬性的詳細資訊，請參閱：

-   [Get 方法](the-get-method.md)
-   [GetEx 方法](the-getex-method.md)
-   [GetInfo 方法](the-getinfo-method.md)
-   [使用 GetInfoEx 的優化](optimization-using-getinfoex.md)
-   [使用 IDirectoryObject 介面存取屬性](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [用於讀取屬性的範例程式碼](example-code-for-reading-attributes.md)

 

 