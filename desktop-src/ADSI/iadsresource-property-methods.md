---
title: 'IADsResource 屬性方法 (Iads .h) '
description: IADsResource 介面的屬性方法會取得或設定下表所述的屬性。 如需屬性方法的一般討論，請參閱介面屬性方法。
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- IADsResource 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d8a9b91030738292d6c2767a85e30d8503508ed44c03e9ffb38b7f797e6bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017169"
---
# <a name="iadsresource-property-methods"></a>IADsResource 屬性方法

[**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)介面的屬性方法會取得或設定下表所述的屬性。 如需屬性方法的一般討論，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**LockCount**
</dt> <dd> <dl>

資源上的鎖定數目。

<dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

**路徑**
</dt> <dd> <dl>

開啟之資源的檔案系統路徑。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

**使用者**
</dt> <dd> <dl>

開啟資源之使用者的名稱。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

**UserPath**
</dt> <dd> <dl>

開啟資源之使用者的使用者物件 ADsPath。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>範例

下列程式碼範例顯示如何檢查檔案服務的開啟資源。


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



下列程式碼範例會列舉資源的集合。


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsResource 定義為34A05B20-4AAB-11CF-AE2C-00AA006EBFB9<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[**IADsFileServiceOperations：： Resources**](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





