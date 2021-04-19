---
description: 永久事件取用者的註冊需要 \_ \_ >eventfilter 系統類別的實例。
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: __EventFilter 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
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
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983724"
---
# <a name="__eventfilter-class"></a>\_\_>eventfilter 類別

永久事件取用者的註冊需要 **\_ \_ >eventfilter** 系統類別的實例。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a>成員

**\_ \_ >eventfilter** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ >eventfilter** 類別具有這些屬性。

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

安全識別碼 (SID) ，可唯一識別建立此篩選器的使用者。 Windows Management Instrumentation (WMI) 會將建立 **\_ \_ >eventfilter** 實例的使用者 sid，或系統管理員 sid 儲存在不同的作業系統上。 如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

</dd> <dt>

**EventAccess**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

安全描述項定義語言中的安全描述項 (SD)  (SDDL) ，可控制傳遞至篩選之事件的存取權。 您可以使用這個屬性來指定只能將特定帳戶之安全性內容中的事件傳遞給此篩選器。 例如，當特定使用者產生特定事件時，永久事件取用者可能會清除安全性記錄。 若要指定可以將事件發佈到此篩選器的使用者，請在 [[**安全 \_ 描述項**](--event.md)] 屬性的 [存取控制] 專案中，使用 [ **WBEM] 右邊的 \_ \_ 發佈** 遮罩 (ACE) 。 如需詳細資訊，請參閱 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)。 如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。 如需詳細資訊和範例，請參閱取代：[安全地接收事件](receiving-events-securely.md)。

您可以設定事件存取安全描述項，只允許在本機系統帳戶產生事件時傳遞事件。 如需建立安全描述項及授權存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。

範例：下列 SDDL 字串只允許系統管理員將事件提供給篩選準則。 提供事件所需的正確之處是 (x80) 的 **WBEM \_ 正確 \_ 發佈** 。


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**EventNamespace**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用於跨命名空間訂閱之事件實例的命名空間。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

事件篩選器的唯一識別碼。 因為事件篩選器只會由 WMI 在內部使用，建議您將此屬性設定為全域唯一識別碼 (**GUID**) 轉換成字串。 不過，取用者可以使用任何私用配置來篩選名稱，只要不會與其他篩選發生衝突。

</dd> <dt>

**查詢**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

Windows Management Instrumentation Query Language (WQL) 事件查詢，該查詢會指定取用者通知的事件組，以及通知的特定條件。

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用於查詢的語言。 因為 WMI 目前僅支援 WMI 查詢語言 (WQL) 作為查詢語言，所以此屬性必須設定為 "WQL"。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ >eventfilter** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)。

## <a name="examples"></a>範例

在 TechNet 資源庫上 [建立永久性 wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2)檔案 PowerShell 範例使用 **\_ \_ >eventfilter** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[建立事件篩選器](creating-an-event-filter.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[監視事件](monitoring-events.md)
</dt> <dt>

[標準取用者類別](standard-consumer-classes.md)
</dt> <dt>

[保護 WMI 事件](securing-wmi-events.md)
</dt> </dl>

 

