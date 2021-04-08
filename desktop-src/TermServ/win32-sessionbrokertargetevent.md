---
title: Win32_SessionBrokerTargetEvent 類別
description: 代表會話 broker 目標的變更。
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent 類別遠端桌面服務
- Win32_SessionBrokerTargetEvent 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685708"
---
# <a name="win32_sessionbrokertargetevent-class"></a>Win32 \_ SessionBrokerTargetEvent 類別

代表會話 broker 目標的變更。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>成員

**Win32 \_ SessionBrokerTargetEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SessionBrokerTargetEvent** 類別具有這些屬性。

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定發生的變更。 這可以是下列其中一個值。

<dt>

1 (0x1) 
</dt> <dd>

未指定變更的類型。

</dd> <dt>

2 (0x2) 
</dt> <dd>

外部 IP 位址已變更。

</dd> <dt>

4 (0x4) 
</dt> <dd>

內部 IP 位址已變更。

</dd> <dt>

8 (0x8) 
</dt> <dd>

目標已聯結。

</dd> <dt>

16 (0x10) 
</dt> <dd>

已移除目標。

</dd> <dt>

32 (0x20) 
</dt> <dd>

目標的狀態已變更。

</dd> <dt>

64 (0x40) 
</dt> <dd>

目標為閒置。

</dd> </dl>

</dd> <dt>

**環境**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

環境名稱。 如果虛擬機器 (VM) 目標，這可能是 VM 主機名稱。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目標所屬伺服器陣列的名稱。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用

</dd> <dt>

**Guid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目標的 GUID。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

外掛程式的名稱。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。 如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目標的名稱。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。 這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

