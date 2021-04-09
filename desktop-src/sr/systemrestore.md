---
title: SystemRestore 類別
description: 提供方法來停用和啟用監視、列出可用的還原點，以及在本機系統上起始還原。
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- SystemRestore 類別系統還原
- SystemRestore 類別系統還原，說明
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025219"
---
# <a name="systemrestore-class"></a>SystemRestore 類別

提供方法來停用和啟用監視、列出可用的還原點，以及在本機系統上起始還原。

## <a name="syntax"></a>語法

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>成員

**SystemRestore** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SystemRestore** 類別有這些方法。



| 方法                                                             | 描述                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | 建立還原點。<br/>                         |
| [**停用**](disable-systemrestore.md)                           | 停用特定磁片磁碟機上的監視。<br/>       |
| [**啟用**](enable-systemrestore.md)                             | 在特定磁片磁碟機上啟用監視。<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | 捕獲上次系統還原的狀態。<br/> |
| [**還原**](restore-systemrestore.md)                           | 起始系統還原。<br/>                      |



 

### <a name="properties"></a>屬性

**SystemRestore** 類別具有這些屬性。

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

發生狀態變更的時間。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要顯示的描述，讓使用者可以輕鬆地識別還原點。 ANSI 字串的最大長度為最大 \_ DESC。 Unicode 字串的最大長度為最大 \_ DESC \_ W。 如需詳細資訊，請參閱 [還原點描述文字](restore-point-description-text.md)。

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

事件的類型。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**開始 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>102</dt> </dl> | 系統變更已開始。 後續的嵌套呼叫不會建立新的還原點。 <br/> 後續呼叫必須使用 END \_ NESTED \_ 系統 \_ 變更，而不是終端 \_ 系統 \_ 變更。<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**開始 \_系統 \_ 變更**</dt> <dt>100</dt> </dl>                       | 系統變更已開始。<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**結束 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>103</dt> </dl>       | 系統變更已結束。<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**結束 \_系統 \_ 變更**</dt> <dt>101</dt> </dl>                             | 系統變更已結束。<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

還原點的類型。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                          | 意義                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**應用程式 \_安裝**</dt> <dt>0</dt> </dl>         | 已安裝應用程式。<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**應用程式 \_卸載**</dt> <dt>1</dt> </dl>   | 已卸載應用程式。<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> 已 <dt>**取消 \_操作**</dt> <dt>13</dt> </dl>        | 應用程式必須刪除它所建立的還原點。 例如，當使用者取消安裝時，應用程式會使用此旗標。 <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**裝置 \_驅動程式 \_ 安裝**</dt> <dt>10</dt> </dl> | 已安裝設備磁碟機。<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**修改 \_設定**</dt> <dt>12</dt> </dl>                    | 應用程式已新增或移除功能。<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

還原點的序號。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用 [**SWbemServices InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) 方法取得還原點的清單，以取得 **SystemRestore** 物件的集合。 您可以使用類別屬性來識別還原點。

## <a name="examples"></a>範例

下列範例腳本會列舉目前的還原點。


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                         |
| 命名空間<br/>                | 根 \\ 預設值<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr-iov</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

