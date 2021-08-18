---
title: 'IADsAcl 屬性方法 (Iads .h) '
description: IADsAcl 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- IADsAcl 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebe534df506bcf25aa618213a4e274500035c8ea8b21941ae4e57a784d26c30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961927"
---
# <a name="iadsacl-property-methods"></a>IADsAcl 屬性方法

[**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**特權**
</dt> <dd> <dl>

許可權設定。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

**ProtectedAttrName**
</dt> <dd> <dl>

受保護屬性的名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

**SubjectName**
</dt> <dd> <dl>

主體的名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsAcl 定義為8452D3AB-0869-11D1-A377-00C04FB950DC<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





