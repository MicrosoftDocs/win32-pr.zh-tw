---
description: 報告實例建立事件，這是在新的實例新增至命名空間時所產生的內建事件種類。
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194719"
---
# <a name="__instancecreationevent-class"></a>\_\_InstanceCreationEvent 類別

**\_ \_ InstanceCreationEvent** 系統類別會報告實例建立事件，這是在新的實例新增至命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ InstanceCreationEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ InstanceCreationEvent** 類別具有這些屬性。

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

所建立之實例的複本。 這個屬性繼承自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 這項資訊是 (UTC) 格式的國際標準時間。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ InstanceCreationEvent** 類別衍生自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。

**建立資源： \_ \_ InstanceCreationEvent**

假設您想要在特定電腦上執行「記事本」時收到通知。 當「記事本」執行時，會建立對應的進程。 您可以使用 WMI 來管理處理程式，並以 Win32 \_ 進程類別來表示。 當「記事本」開始執行時，Win32 進程類別的對應實例 \_ 會變成可透過 WMI 使用。 如果您已在此事件 (註冊適當的事件通知查詢) ，此實例的可用性會導致建立 **\_ \_ InstanceCreationEvent** 類別的實例。

要求建立資源和使用內建事件之通知的通知查詢，全都使用類似下面的語法：

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

如需使用 **\_ \_ InstanceCreationEvent** 作為監視檔案系統之方法的更大討論，請參閱 CodeProject 上的 [WMI 和檔案系統監視](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring)。

## <a name="examples"></a>範例

在 TechNet 資源庫上 [建立永久性 wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2)檔案 PowerShell 範例使用 **\_ \_ InstanceCreationEvent** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。

TechNet 資源庫上的 [powershell WMI 永久事件](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262)powershell 範例會使用 **\_ \_ InstanceCreationEvent** 做為設定永久事件註冊的示範腳本的一部分。

TechNet 上的 [監視器進程建立事件](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d)VBScript 範例使用 **\_ \_ InstanceCreationEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的第一個 WMI 實例建立事件。

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

 

