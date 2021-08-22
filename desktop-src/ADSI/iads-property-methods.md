---
title: 'IADs 屬性方法 (Iads .h) '
description: IADs 介面的屬性方法會取得或設定下表所述的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- IADs 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3326bbbf5ea7c2d2a98a6224f9b0a83a738c76a206d343a8629138d4d45e73b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082522"
---
# <a name="iads-property-methods"></a>IADs 屬性方法

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面的屬性方法會取得或設定下表所述的屬性。 如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

這個物件的 ADsPath 字串。 此字串可在網路環境中唯一識別此物件。 您一律可以使用此路徑來抓取物件。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**類別**
</dt> <dd> <dl>

物件架構類別的名稱。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

目錄物件的全域唯一識別碼。 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面會將 **GUID** 從儲存在目錄伺服器上的八位字串轉換成字串格式。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**名稱**
</dt> <dd> <dl>

在基礎目錄服務中命名之物件的相對名稱。 此名稱會區分這個物件與其同級。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**父系**
</dt> <dd> <dl>

父容器的 ADsPath 字串。 Active Directory 不允許藉由串連 **Parent** 和 **Name** 屬性來構成指定物件的 ADsPath。 雖然這項作業可能適用于某些提供者，但不保證適用于所有的執行。 ADsPath 保證是有效的，而且應該一律用來取出物件的介面指標。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**結構描述**
</dt> <dd> <dl>

這個物件的架構類別物件的 ADsPath 字串。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

在 Active Directory 中，GUID 傳回的 **guid** 是 hexadecimals 的字串。 使用結果 **GUID** 直接系結至物件。


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



其中 xxx 是從 GUID 屬性傳回的值。 如需詳細資訊，請參閱 [使用 objectGUID 系結至物件](/windows/desktop/AD/using-objectguid-to-bind-to-an-object)。 請注意，如果您使用 GUID 來系結至物件，則 **ADsPath** 屬性方法會傳回不同于一般值的值，如果您使用 (DN) 的分辨名稱來系結至相同物件，則會傳回這些值。 例如，下表列出使用兩個不同的系結方法系結至相同的使用者物件時，所傳回的值。



|             | 使用 DN 系結                                           | 使用 GUID 系結                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **名稱**    | CN = Jeff Smith                                           | CN = Jeff Smith                                               |
| **父系**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://server/CN=Jeff Smith，CN = Users，DC = Fabrikam，DC = com | LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> WinNT 提供者不支援使用物件 **GUID** 進行系結，並以稍微不同的字串格式傳回 **GUID** 屬性。

 

## <a name="examples"></a>範例

下列程式碼範例示範如何使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的屬性方法來取出物件資料。


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



下列程式碼範例示範如何使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的屬性方法來取出物件資料。


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



下列程式碼範例顯示如何使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的屬性方法。


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADs 定義為 FD8256D0-FD15-11CE-ABC4-02608C9E7553<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

