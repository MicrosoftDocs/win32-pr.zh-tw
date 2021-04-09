---
title: Modify MicrosoftDNS_WKSType 類別的方法
description: Modify 方法會) 資源記錄更新 Well-Known Services (WKS。
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_WKSType 類別
- MicrosoftDNS_WKSType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843860"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Modify MicrosoftDNS \_ WKSType 類別的方法

**Modify** 方法會) 資源記錄更新 Well-Known SERVICES (WKS。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*InternetAddress* \[在中，選擇性\]
</dt> <dd>

記錄擁有者的網際網路 IP 位址。

</dd> <dt>

*IPProtocol* \[在中，選擇性\]
</dt> <dd>

代表此記錄之 IP 通訊協定的字串。 有效的值為 UDP 或 TCP。

</dd> <dt>

*服務* \[在中，選擇性\]
</dt> <dd>

字串，其中包含已知服務 (WKS) 記錄所使用的所有服務。

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**MicrosoftDNS WKSType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





