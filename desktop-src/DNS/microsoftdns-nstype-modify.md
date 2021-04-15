---
title: Modify MicrosoftDNS_NSType 類別的方法
description: Modify 方法會更新名稱伺服器 (NS) 資源記錄。
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_NSType 類別
- MicrosoftDNS_NSType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3dd26b7c0f1c31ef3ea742f20f70df8646a087b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467097"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a>Modify MicrosoftDNS \_ NSType 類別的方法

**Modify** 方法會更新名稱伺服器 (NS) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*NSHost* \[在中，選擇性\]
</dt> <dd>

網域的授權主機。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

修改過之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

任何未指定的參數在修改過的記錄中都會保持不變。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)
</dt> <dt>

[**MicrosoftDNS PTRType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





