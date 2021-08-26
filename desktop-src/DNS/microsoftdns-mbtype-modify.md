---
title: Modify MicrosoftDNS_MBType 類別的方法
description: Modify 方法會更新信箱 (MB) 資源記錄。
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MBType 類別
- MicrosoftDNS_MBType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b0e4183a2b736d0ed896fee4bf2cc57e35f0e6b628a9aee4345f4c33b33ed6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918338"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a>Modify MicrosoftDNS \_ MBType 類別的方法

**Modify** 方法會更新信箱 (MB) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*MBHost* \[在\]
</dt> <dd>

表示 MB 記錄之信箱主機名稱的字串。

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

[**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)
</dt> <dt>

[**MicrosoftDNS MBType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





