---
title: MicrosoftDNS_X25Type 類別
description: '\_代表 (X25) 記錄之 MicrosoftDNS ResourceRecord 的子類別。'
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- MicrosoftDNS_X25Type 類別 DNS
- MicrosoftDNS_X25Type 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969183"
---
# <a name="microsoftdns_x25type-class"></a>MicrosoftDNS \_ X25Type 類別

代表 (X25) 記錄之 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 的子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ X25Type** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ X25Type** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法輸入參數中的資料具現化 RR 的 ' X25 ' 類型：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值和 PSDN 位址。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/>              |
| **修改**                         | 這個方法會將 TTL 和 PSDN 位址更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/> |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ X25Type** 類別具有這些屬性。

<dl> <dt>

**PSDNAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RR 擁有者的 PSDN 位址。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS X25Type 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ X25Type 類別的方法**](microsoftdns-x25type-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





