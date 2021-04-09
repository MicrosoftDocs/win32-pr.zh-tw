---
description: 報告實例修改事件，這是在命名空間中的實例變更時所產生的內建事件種類。
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850788"
---
# <a name="__instancemodificationevent-class"></a>\_\_InstanceModificationEvent 類別

**\_ \_ InstanceModificationEvent** 系統類別會報告實例修改事件，這是在命名空間中的實例變更時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ InstanceModificationEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ InstanceModificationEvent** 類別具有這些屬性。

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

修改之前的實例複本。

</dd> <dt>

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

已變更之實例的新版本。 這個屬性繼承自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。

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

**\_ \_ InstanceModificationEvent** 類別衍生自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。

**修改資源： \_ \_ InstanceModificationEvent**

假設您懷疑正在使用的管理應用程式，在您的其中一部伺服器上錯誤地變更服務的啟動類型。 您想要撰寫 WMI 腳本來監視對服務的設定所做的任何修改。 一旦對服務進行修改，其對應的 TargetInstance 就會反映修改。

如果您在此活動中註冊您的興趣，則修改服務的設定會導致建立 **\_ \_ InstanceModificationEvent** 類別的實例。

要求修改資源和使用內建事件的通知查詢，全都使用類似下面的語法：

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>範例

TechNet 資源庫上的 [監視器進程修改事件](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079)VBScript 範例會使用 **\_ \_ InstanceModificationEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)第一次出現的 WMI 實例修改事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

