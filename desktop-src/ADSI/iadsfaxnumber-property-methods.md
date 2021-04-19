---
title: 'IADsFaxNumber 屬性方法 (Iads .h) '
description: IADsFaxNumber 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- IADsFaxNumber 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966333"
---
# <a name="iadsfaxnumber-property-methods"></a>IADsFaxNumber 屬性方法

[**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**參數**
</dt> <dd> <dl>

傳真電腦的參數。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

**TelephoneNumber**
</dt> <dd> <dl>

傳真電腦的電話號碼。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
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
| IID<br/>                      | IID \_ IADsFaxNumber 定義為 A910DEA9-4680-11D1-0A3B-00C04FB950DC<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[**ADS \_ FAXNUMBER**](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





