---
title: Modify MicrosoftDNS_WINSType 類別的方法
description: Modify 方法會更新 Windows 網際網路名稱服務 (WINS) 資源記錄。
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_WINSType 類別
- MicrosoftDNS_WINSType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843867"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Modify MicrosoftDNS \_ WINSType 類別的方法

**Modify** 方法會更新 Windows 網際網路名稱服務 (WINS) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*MappingFlag* \[在中，選擇性\]
</dt> <dd>

WINS 對應旗標，指定是否必須將記錄包含在區域複寫中。 它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。 下列是有效的值。



| 值                                                                                                                                               | 意義                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | 複寫旗標<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | 無複寫 (本機記錄) 旗標<br/> |



 

</dd> <dt>

*LookupTimeout* \[在中，選擇性\]
</dt> <dd>

DNS 伺服器使用 WINS 查詢來嘗試解析的時間（以秒為單位）。

</dd> <dt>

*CacheTimeout* \[在中，選擇性\]
</dt> <dd>

使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。

</dd> <dt>

*WinsServers* \[在中，選擇性\]
</dt> <dd>

WINS 查詢中使用之 WINS 伺服器的逗點分隔 IP 位址清單。

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

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**MicrosoftDNS WINSType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





