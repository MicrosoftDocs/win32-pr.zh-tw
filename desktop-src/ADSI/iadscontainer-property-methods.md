---
title: 'IADsContainer 屬性方法 (Iads .h) '
description: IADsContainer 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，以及有關屬性方法的一般討論，請參閱介面屬性方法。
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- IADsContainer 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13515bcf90c926db839aad60d49599967ee0d24bedbe0deb4b7d1d21c3c016e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428083"
---
# <a name="iadscontainer-property-methods"></a>IADsContainer 屬性方法

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，以及有關屬性方法的一般討論，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**Count**
</dt> <dd> <dl>

捕獲容器中的專案數。 當設定 **篩選準則** 時， **Count** 只會傳回篩選的專案數目。

<dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

抓取或設定篩選準則，用來選取指定列舉中的物件類別。 這是 variant 陣列，其中的每個元素都是架構類別的名稱。 如果 **篩選** 未設定或設為空白，則列舉值會抓取所有類別的所有物件。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

**提示**
</dt> <dd> <dl>

**BSTR** 字串的 variant 陣列。 每個元素都會識別在架構定義中找到的屬性名稱。 *VHints* 參數可讓用戶端指定要為每個列舉物件載入哪些屬性。 您可以使用這類資料來優化網路存取。 但是，確切的實作為提供者特有的，而且目前不是由 WinNT 提供者所使用。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

[**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)和 **IADsContainer：： get \_ Count** 下的列舉進程會針對快取中的包含物件執行。 當容器包含大量物件時，效能可能會受到影響。 若要增強效能，請關閉快取、設定適當的頁面大小，然後使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面。 基於這個理由，Microsoft LDAP 提供者不支援 **get \_ Count** 屬性。

## <a name="examples"></a>範例

下列 Visual Basic 程式碼範例會示範如何使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)的屬性方法。


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



下列 c + + 程式碼範例會顯示如何使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 的屬性方法。 為了簡潔起見，會忽略錯誤檢查。


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer 定義為001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





