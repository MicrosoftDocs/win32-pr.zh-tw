---
title: Win32_CentralPublishingChangeEvent 類別
description: 代表中央 RDV 設定變更的事件。
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent 類別遠端桌面服務
- Win32_CentralPublishingChangeEvent 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc38d132920bd5ffcaa2208d8f1aa94c8629bb0c5399f6b8776654d078cd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868518"
---
# <a name="win32_centralpublishingchangeevent-class"></a>Win32 \_ CentralPublishingChangeEvent 類別

代表中央 RDV 設定變更的事件。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a>成員

**Win32 \_ CentralPublishingChangeEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ CentralPublishingChangeEvent** 類別具有這些屬性。

<dl> <dt>

**OperationType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對應至事件的作業類型。

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**建立** (0) 


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

**修改** (1) 


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

**刪除** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。 如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

由對應至事件的作業所變更的物件。

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
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                           |
| 命名空間<br/>                | 根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

