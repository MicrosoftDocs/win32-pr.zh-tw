---
description: 作為與實例相關之所有內建事件的基類。
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975272"
---
# <a name="__instanceoperationevent-class"></a>\_\_InstanceOperationEvent 類別

**\_ \_ InstanceOperationEvent** 系統類別可做為與實例相關之所有內部事件的基類。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ InstanceOperationEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ InstanceOperationEvent** 類別具有這些屬性。

<dl> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

受事件影響的實例。 針對建立事件，這是新建立的實例。 針對修改事件，這是已變更之實例的新版本。 如果是刪除事件，這就是已刪除的實例。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ InstanceOperationEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。

不會建立 **\_ \_ InstanceOperationEvent** 的實例，只會建立其子類別的實例。 下列類別衍生自 **\_ \_ InstanceOperationEvent**：

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**概觀**

就像 WMI 類別一樣，它代表可使用 WMI 管理的每種系統資源類型，有一個 WMI 類別代表每個 WMI 事件種類。 當 WMI 可以監視的事件發生時，就會建立對應 WMI 事件類別的實例。 建立實例時，就會發生 WMI 事件。

Wmi 事件類別共有三種主要類型，這些類別都是衍生自 [**\_ \_ 事件**](--event.md)WMI 類別：內部事件、外建事件和計時器事件。 內建事件接著會以三個衍生自 **\_ \_ 事件** 類別的不同類別來表示： [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)、 **\_ \_ InstanceOperationEvent** 和 [**\_ \_ ClassOperationEvent**](--classoperationevent.md)。

內建事件

內建事件是用來監視 CIM 存放庫中的類別所代表的資源。 每個資源都會以類別的實例來表示。 這表示使用 WMI 監視資源其實牽涉到監視對應至資源的實例。

內建事件也可以用來監視儲存機制中的命名空間或類別的變更。 不過，監視命名空間或類別的變更對於系統管理員而言的價值有限。

內建事件是以衍生自 \_ \_ InstanceOperationEvent、 \_ \_ NamespaceOperationEvent 或 \_ \_ ClassOperationEvent 之類別的實例來表示。 對 WMI 中的實例所做的任何變更，都會以 \_ \_ InstanceOperationEvent 類別和衍生自它的類別來表示： \_ \_ InstanceCreationEvent、 \_ \_ InstanceModificationEvent 和 \_ \_ InstanceDeletionEvent。

使用 WMI 監視資源涉及監視實例，而實例的所有變更都會以 \_ \_ InstanceOperationEvent 和衍生自它的類別來表示。 這表示監視資源最後牽涉到監視 \_ \_ InstanceOperationEvent 衍生類別的實例。

您可以發出以 WQL 表示的通知查詢，在其中一個類別的實例中註冊感興趣的人。 查詢使用類似下面的語法：

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

如需使用 WMI 實例事件來監視電腦活動的更長討論，請參閱 [如何使用單一腳本來監視不同類型的事件？](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>範例

TechNet 資源庫上的 [監視器進程事件](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f)VBScript 程式碼範例會使用 **\_ \_ InstanceOperationEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的第一個 WMI 實例事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_事件**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[根據事件寫入記錄檔](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

