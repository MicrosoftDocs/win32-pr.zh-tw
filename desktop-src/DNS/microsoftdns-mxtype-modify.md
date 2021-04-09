---
title: Modify MicrosoftDNS_MXType 類別的方法
description: Modify 方法會將郵件交換程式更新 (MR) 資源記錄。
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MXType 類別
- MicrosoftDNS_MXType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935051"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Modify MicrosoftDNS \_ MXType 類別的方法

**Modify** 方法會將郵件交換程式更新 (MR) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*喜好* \[ 設定在中，選擇性\]
</dt> <dd>

在相同擁有者的其他專案中提供給此 RR 的喜好設定。 偏好較低的值。

</dd> <dt>

*MailExchange* \[在中，選擇性\]
</dt> <dd>

FQDN 指定的主機願意作為擁有者名稱的郵件交換。

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

[**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)
</dt> <dt>

[**MicrosoftDNS MXType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





