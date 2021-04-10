---
title: MicrosoftDNS_NXTType 類別
description: '\_表示下一個 (NXT) RR 的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- MicrosoftDNS_NXTType 類別 DNS
- MicrosoftDNS_NXTType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104165"
---
# <a name="microsoftdns_nxttype-class"></a>MicrosoftDNS \_ NXTType 類別

表示下一個 (NXT) RR 的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ NXTType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ NXTType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 NXT 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時，以及要附加的功能變數名稱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/>                                                                                                                                           |
| **修改**                         | 將 TTL、對應旗標、查閱超時、快取超時和結果網域更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/> **Windows Server 2003：** 這個方法也會將 NextDomainName 和類型更新為指定為此方法之輸入參數的值。<br/> <br/> |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ NXTType** 類別具有這些屬性。

<dl> <dt>

**NextDomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

下一個功能變數名稱。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

針對 NXT 資源記錄的擁有者名稱，以空格分隔的 RR 類型助憶鍵清單。

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

[**MicrosoftDNS NXTType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ NXTType 類別的方法**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





