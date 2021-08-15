---
title: Modify MicrosoftDNS_ATMAType 類別的方法
description: Modify 方法會將 ATM 位址更新為 (ATMA) 資源記錄的名稱。
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_ATMAType 類別
- MicrosoftDNS_ATMAType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c8f98288c519340e6a95959964a4c42799201c7e1701bb748f634746a94226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163756"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Modify MicrosoftDNS \_ ATMAType 類別的方法

**Modify** 方法會將 ATM 位址更新為 (ATMA) 資源記錄的名稱。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*格式* \[在中，選擇性\]
</dt> <dd>

ATM 位址格式。 格式有兩個可能的值：0表示 ATM 終端系統位址 (AESA) 格式，而1表示電子164格式。

</dd> <dt>

*ATMAddress* \[在中，選擇性\]
</dt> <dd>

包含此 RR 所屬節點/擁有者之 ATM 位址的八位變數長度字串。 陣列的前四個位元組是用來儲存八位字串的大小。 最重要的位元組會儲存在位元組0中。

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

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**MicrosoftDNS ATMAType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





