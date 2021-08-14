---
title: Modify MicrosoftDNS_NXTType 類別的方法
description: Modify 方法會更新下一個 (NXT) 資源記錄。
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_NXTType 類別
- MicrosoftDNS_NXTType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43082ff829a7b8701701e9b099aa0f36d274879bfb6f281272096558f1c8bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163199"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Modify MicrosoftDNS \_ NXTType 類別的方法

**Modify** 方法會更新下一個 (NXT) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*NextDomainName* \[在\]
</dt> <dd>

下一個功能變數名稱。

</dd> <dt>

*類型* \[在\]
</dt> <dd>

針對 NXT 資源記錄的擁有者名稱，以空格分隔的 RR 類型助憶鍵清單。

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

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**MicrosoftDNS NXTType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





