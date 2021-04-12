---
title: MicrosoftDNS_SRVType 類別
description: '\_代表服務 (SRV) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType 類別 DNS
- MicrosoftDNS_SRVType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465673"
---
# <a name="microsoftdns_srvtype-class"></a>MicrosoftDNS \_ SRVType 類別

代表服務 (SRV) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ SRVType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ SRVType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 SRV 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/目標名稱、類別 (預設值 = IN) 、存留時間值，以及目標主機的優先順序、權數、埠和功能變數名稱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **修改**                         | 將 TTL、優先順序、權數、埠和功能變數名稱更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                  |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ SRVType** 類別具有這些屬性。

<dl> <dt>

**通訊埠**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

通訊協定服務的目標主機上所使用的埠。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

擁有者名稱中指定的目標主機優先權。 數位下限表示較高的優先順序。

</dd> <dt>

**SRVDomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目標主機的 FQDN。 的目標 \\ 。 \\ 表示此網域無法使用由於原子服務。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目標主機的加權。 在具有相同優先順序的主機之間進行選取時，這非常有用。 使用此主機的機率應與其權數成正比。

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

[**MicrosoftDNS SRVType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ SRVType 類別的方法**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





