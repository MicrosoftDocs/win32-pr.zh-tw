---
title: Modify MicrosoftDNS_MFType 類別的方法
description: Modify 方法會更新網域 (MF) 資源記錄的郵件轉送代理程式。
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MFType 類別
- MicrosoftDNS_MFType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa387e067678299c14f3925299d1bdb658ec010458f81ecac3727bf8bf9aa3c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874918"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a>Modify MicrosoftDNS \_ MFType 類別的方法

**Modify** 方法會更新網域 (MF) 資源記錄的郵件轉送代理程式。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*MFHost* \[在中，選擇性\]
</dt> <dd>

提供郵件轉送代理程式的主控制項名稱。

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

[**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)
</dt> <dt>

[**MicrosoftDNS MFType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





