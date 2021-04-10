---
title: Modify MicrosoftDNS_ISDNType 類別的方法
description: Modify 方法會更新 ISDN 資源記錄。
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_ISDNType 類別
- MicrosoftDNS_ISDNType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933943"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a>Modify MicrosoftDNS \_ ISDNType 類別的方法

**Modify** 方法會更新 ISDN 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*ISDNNumber* \[在中，選擇性\]
</dt> <dd>

記錄擁有者的 ISDN 號碼和 DDI。

</dd> <dt>

子 *位址* \[在中，選擇性\]
</dt> <dd>

擁有者的子位址（若已定義）。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

新物件的參考。

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

[**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)
</dt> <dt>

[**MicrosoftDNS ISDNType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





