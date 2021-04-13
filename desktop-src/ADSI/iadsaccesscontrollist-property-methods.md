---
title: 'IADsAccessControlList 屬性方法 (Iads .h) '
description: IADsAccessControlList 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: cb68bb61-4216-4f69-bea1-ab7f98937a27
ms.tgt_platform: multiple
keywords:
- IADsAccessControlList 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlList Property Methods
- IADsAccessControlList.AclRevision
- IADsAccessControlList.get_AclRevision
- IADsAccessControlList.put_AclRevision
- IADsAccessControlList.AceCount
- IADsAccessControlList.get_AceCount
- IADsAccessControlList.put_AceCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55763b7c52071ca5bfd0a875912941090b7992c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384134"
---
# <a name="iadsaccesscontrollist-property-methods"></a>IADsAccessControlList 屬性方法

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**AceCount**
</dt> <dd> <dl>

存取控制清單中的存取控制專案數目。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceCount(
  [out] LONG* lnAceCount
);
HRESULT put_AceCount(
  [in] LONG lnAceCount
);
```


</dt> </dl> </dd> <dt>

**AclRevision**
</dt> <dd> <dl>

存取控制清單的修訂層級。 此值可以是 **acl \_ 修訂** 或 **acl \_ 修訂 \_ DS**。 如果 ACL 包含特定物件的 ACE，請使用 **acl \_ 修訂 \_ DS** 。 ACL 中的所有 Ace 都必須位於相同的修訂層級。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AclRevision(
  [out] LONG* lnAclRevision
);
HRESULT put_AclRevision(
  [in] LONG lnAclRevision
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>範例

下列程式碼範例會顯示 ACL 中的 Ace 數目。


```VB
Dim x as IADs
Dim sd As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList

On Error GoTo Cleanup

Set x = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
Debug.Print Dacl.AceCount

Cleanup:
    If (Err.Number <> 0) Then
        MsgBox ("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
```



下列程式碼範例會顯示 ACL 中的 Ace 數目。


```C++
HRESULT ShowACEInACL(LPWSTR guestPath,LPWSTR user,LPWSTR passwd)
{
  IADs *pObj = NULL;
  IADsSecurityDescriptor *psd = NULL;
  HRESULT hr = S_OK;
  VARIANT var;

  VariantInit(&var);

  hr = ADsOpenObject(guestPath,user,passwd,ADS_SECURE_AUTHENTICATION,
                     IID_IADs,(void**)&pObj);
  if(FAILED(hr)) {
      printf("hr = %x\n",hr);
      return hr;
  }
  else {
      BSTR bstr = NULL;
      pObj->get_Class(&bstr);
      printf("Object class: %S\n",bstr);
      SysFreeString(bstr);
  }

  hr = pObj->Get(CComBSTR("ntSecurityDescriptor"), &var);
  pObj->Release();

  if(FAILED(hr)) {
      printf("Get ntSD: hr = %x\n",hr);
      return hr;
  }

  hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor,
                                        (void**)&psd);

  if(FAILED(hr)) {
      printf("DISP: hr = %x\n",hr);
      VariantClear(&var);
      return hr;
  }

  IDispatch *pDisp = NULL;
  hr = psd->get_DiscretionaryAcl(&pDisp);
  VariantClear(&var);

  if(FAILED(hr)) {
      printf("get_DACL : hr = %x\n",hr);
      return hr;
  }

  IADsAccessControlList *pAcl = NULL;
  hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pAcl);
  pDisp->Release();

  if(FAILED(hr)) {
      printf("QI ACL: hr = %x\n",hr);
      return hr;
  }

  long count = 0;
  hr = pAcl->get_AceCount(&count);
  pAcl->Release();
  if(FAILED(hr)) {
      printf("Count: hr = %x\n",hr);
      return hr;
  }

  printf("AceCount = %d\n",count);

  return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsAccessControlList 定義為 B7EE91CC-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

