---
title: Modify MicrosoftDNS_PTRType 類別的方法
description: Modify 方法會更新 PTR) 資源記錄 (的指標。
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_PTRType 類別
- MicrosoftDNS_PTRType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbda85610e34fa6208bac5f8b9ba196be1b24fcadf8a53d87cea627718e9bd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432819"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a>Modify MicrosoftDNS \_ PTRType 類別的方法

**Modify** 方法會更新 PTR) 資源記錄 (的指標。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*PTRDomainName* \[在中，選擇性\]
</dt> <dd>

PTR 記錄的功能變數名稱位址。

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

 

 





