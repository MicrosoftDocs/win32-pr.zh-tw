---
title: Modify MicrosoftDNS_SRVType 類別的方法
description: Modify 方法會更新 (SRV) 資源記錄的服務。
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_SRVType 類別
- MicrosoftDNS_SRVType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025427"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Modify MicrosoftDNS \_ SRVType 類別的方法

**Modify** 方法會更新 (SRV) 資源記錄的服務。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*優先順序* \[在中，選擇性\]
</dt> <dd>

擁有者名稱中指定的目標主機優先權。 數位下限表示較高的優先順序。

</dd> <dt>

*權數* \[在中，選擇性\]
</dt> <dd>

目標主機的加權。 在具有相同優先順序的主機之間進行選取時，這非常有用。 使用此主機的機率應與其權數成正比。

</dd> <dt>

*埠* \[在中，選擇性\]
</dt> <dd>

通訊協定服務的目標主機上所使用的埠。

</dd> <dt>

*SRVDomainName* \[在中，選擇性\]
</dt> <dd>

目標主機的 FQDN。 的目標 \\ 。 \\ 表示此網域無法使用由於原子服務。

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

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**MicrosoftDNS SRVType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





