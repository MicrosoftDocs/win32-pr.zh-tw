---
title: MicrosoftDNS_ATMAType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示用來命名 (ATMA) 記錄的 ATM 位址。
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- MicrosoftDNS_ATMAType 類別 DNS
- MicrosoftDNS_ATMAType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934382"
---
# <a name="microsoftdns_atmatype-class"></a>MicrosoftDNS \_ ATMAType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示用來命名 (ATMA) 記錄的 ATM 位址。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ ATMAType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ ATMAType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 ATMA 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者/節點名稱、類別 (預設值 = IN) 、存留時間值，以及 ATM 格式和位址。 將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **修改**                         | 將 TTL、格式和 ATMA 位址更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>         |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ ATMAType** 類別具有這些屬性。

<dl> <dt>

**ATMAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含此 RR 所屬節點/擁有者之 ATM 位址的八位變數長度字串。 陣列的前4個位元組會用來儲存八位字串的大小。 最重要的位元組會儲存在位元組0中。

</dd> <dt>

**格式**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

ATM 位址格式。 有效的值為：0，表示 ATM 終端系統位址 (AESA) 格式，1表示格式為164。

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

[**MicrosoftDNS ATMAType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ ATMAType 類別的方法**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





