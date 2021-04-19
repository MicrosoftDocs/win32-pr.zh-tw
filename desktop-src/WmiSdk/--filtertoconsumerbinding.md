---
description: 用於註冊永久事件取用者，以便將 EventConsumer 的實例與 >eventfilter 的實例產生關聯 \_ \_ \_ \_ 。
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985491"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_FilterToConsumerBinding 類別

**\_ \_ FilterToConsumerBinding** 系統類別用於註冊永久事件取用者，以便將 [**\_ \_ EventConsumer**](--eventconsumer.md)的實例與 [**\_ \_ >eventfilter**](--eventfilter.md)的實例產生關聯。**\_ \_FilterToConsumerBinding** 是關聯類別。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a>成員

**\_ \_ FilterToConsumerBinding** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ FilterToConsumerBinding** 類別具有這些屬性。

<dl> <dt>

**消費者**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ EventConsumer**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

[**\_ \_ EventConsumer**](--eventconsumer.md)實例的參考，代表邏輯取用者的物件路徑，也就是事件的收件者。 邏輯取用者是衍生自 **\_ \_ EventConsumer** 之類別的實例。

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

安全識別碼 (SID) ，可唯一識別建立系結的使用者。 根據作業系統，WMI 會儲存系統管理員 sid 或建立 **\_ \_ FilterToConsumerBinding** 實例之使用者的 sid。 如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

</dd> <dt>

**DeliverSynchronously**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

已過時。 請改為使用 **DeliveryQoS** 屬性來取代這個屬性，因為如果 **DeliverSynchronously** 設定為 **True** ，則會覆寫 **DeliveryQoS** 屬性的設定。

</dd> <dt>

**DeliveryQoS**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

訂用帳戶的服務品質。 如果 **DeliverSynchronously** 屬性設定為 **True**，它會覆寫 **DeliveryQoS** 屬性的設定。

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_旗標 \_ QOS \_ 同步** (0) 


</dt> <dd>

同步傳遞

**False**： 事件會以同步方式傳遞給邏輯取用者。

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_標示 \_ QOS \_ EXPRESS** (1) 


</dt> <dd>

快遞

**True**。 事件會以非同步方式傳遞給邏輯取用者。

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ >eventfilter**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

[**\_ \_ >eventfilter**](--eventfilter.md)實例的參考，代表事件篩選器的物件路徑，這是指定要接收之事件種類的查詢。

</dd> <dt>

**MaintainSecurityCoNtext**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 True**，則會以提供者提供的相同安全性內容來傳遞事件。

> [!Note]  
> 只有實作為 DLL 的取用者 (同進程取用者) 可以接收提供者之安全性內容中的事件。 如需有關同進程提供者和安全性的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。 如需詳細資訊和範例，請參閱取代：[安全地接收事件](receiving-events-securely.md)。

 

</dd> <dt>

**SlowDownProviders**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 True**，則在此取用者無法趕上時，提供者會變慢。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ FilterToConsumerBinding** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。

永久事件取用者會使用 **\_ \_ FilterToConsumerBinding** 系統類別，將事件篩選器系結至最終取用者。 將篩選和取用者系結在一起之後，WMI 可以將符合篩選準則的事件轉送到對應的取用者。

## <a name="examples"></a>範例

在 TechNet 資源庫上 [建立永久性 wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2)檔案 PowerShell 範例使用 **\_ \_ FilterToConsumerBinding** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_IndicationRelated**](--indicationrelated.md)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[監視事件](monitoring-events.md)
</dt> <dt>

[建立事件篩選器](creating-an-event-filter.md)
</dt> <dt>

[保護 WMI 事件](securing-wmi-events.md)
</dt> </dl>

 

 




