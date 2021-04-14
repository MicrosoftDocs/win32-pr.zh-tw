---
title: SystemRestoreConfig 類別
description: 提供屬性來控制排程的還原點建立頻率，以及每個磁片磁碟機上耗用的磁碟空間量。
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- SystemRestoreConfig 類別系統還原
- SystemRestoreConfig 類別系統還原，說明
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384845"
---
# <a name="systemrestoreconfig-class"></a>SystemRestoreConfig 類別

提供屬性來控制排程的還原點建立頻率，以及每個磁片磁碟機上耗用的磁碟空間量。

## <a name="syntax"></a>語法

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>成員

**SystemRestoreConfig** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemRestoreConfig** 類別具有這些屬性。

<dl> <dt>

**DiskPercent**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統還原可使用的每個磁片磁碟機上的最大磁碟空間量。 此值會指定為總磁片磁碟機空間的百分比。 預設值為12%。

**Windows Vista：** 從磁碟區陰影複製服務 (VSS) 接收值。 這是系統還原可使用的每個磁片磁碟機上的最大磁碟空間量。 預設值是總磁片磁碟機空間的15% 或可用空間的百分之30，以較小者為准。

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

排程的系統檢查點建立的絕對時間間隔（以秒為單位）。 預設值為 86400 (24 小時) 。

**Windows Vista：** 從工作排程器接收系統還原的值。 如果工作已停用，則為零。

</dd> <dt>

**RPLifeInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

保留還原點的時間間隔（以秒為單位）。 當還原點變得超過此指定的間隔時，便會將其刪除。 預設的存留期限制為90天。

**Windows Vista：** 接收 **UINTMAX** 的值。

</dd> <dt>

**RPSessionInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在會話期間建立排程系統檢查點的時間間隔（以秒為單位）。 預設值為零，表示此功能已關閉。

**Windows Vista：** 如果系統還原已停用，則接收零。

</dd> </dl>

## <a name="examples"></a>範例

不支援下列範例程式碼。 使用命令列工具 Vssadmin.exe 來變更保留磁片磁碟機空間的大小。

**WINDOWS XP：** 支援此範例。


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
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

[還原點](restore-points.md)
</dt> <dt>

[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

