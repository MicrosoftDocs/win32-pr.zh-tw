---
title: Modify MicrosoftDNS_AFSDBType 類別的方法
description: Modify 方法會更新 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_AFSDBType 類別
- MicrosoftDNS_AFSDBType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966113"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Modify MicrosoftDNS \_ AFSDBType 類別的方法

**Modify** 方法會更新 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*子類型* \[在中，選擇性\]
</dt> <dd>

主機 AFS 伺服器的子類型。 針對子類型 1 (值 = 1) ，主機具有適用于已命名 AFS 資料格的 AFS 3.0 磁片區位置伺服器。 在子類型 2 (值 = 2) 的情況下，主機會有經過驗證的名稱伺服器，保留命名的 DCE/NCA 資料格的資料格根目錄節點。

</dd> <dt>

*ServerName* \[在中，選擇性\]
</dt> <dd>

FQDN 指定主機，該主機的擁有者名稱中指定的 AFS 資料格具有伺服器。

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**MicrosoftDNS AFSDBType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





