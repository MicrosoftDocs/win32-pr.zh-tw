---
title: CHANGE_LOG_ENTRY 結構
description: 變更記錄專案。
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- CHANGE_LOG_ENTRY 結構系統還原
- PCHANGE_LOG_ENTRY 結構指標系統還原
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee4eca1bad0859159821d7717ba6c23c352e03b33a1fcab81721e08dba465c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452929"
---
# <a name="change_log_entry-structure"></a>變更 \_ 記錄 \_ 專案結構

\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]

變更記錄專案。

## <a name="syntax"></a>語法


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**RecordHeader**
</dt> <dd>

[**記錄 \_ 標頭**](record-header.md)結構。 **DwRecordType** 成員應設定為 **RecordTypeLogEntry** (1) 。

</dd> <dt>

**dwMagicNum**
</dt> <dd>

此成員應設定為0xabcdef12。

</dd> <dt>

**dwEntryType**
</dt> <dd>

這個成員可以是下列其中一個值：

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ACLCHANGE * * (0x2) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ATTRCHANGE * * (0x4) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ DIRCREATE * * (0x80) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ DIRRENAME * * (0x100) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ DIRDELETE * * (0x200) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ FILECREATE * * (0x20) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ FILEDELETE * * (0x10) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ FILERENAME * * (0x40) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ INPRECREATE * * (0x100000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ISDIR * * (0x20000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ISNOTDIR * * (0x40000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ MOUNTCREATE * * (0x400) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ MOUNTDELETE * * (0x800) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ NOOPTIMIZE * * (0x10000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ OPENBYID * * (0x200000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ SIMULATEDELETE * * (0x80000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMCHANGE * * (0x1) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMCREATE * * (0x2000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMOVERWRITE * * (0x8) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ VOLUMEERROR * * (0x1000) * *
</dt> </dl> </dd> <dt>

**dwEntryFlags**
</dt> <dd>

這個成員可以是下列其中一個值：

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ ACLINFO (0x4)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ DEBUGINFO (0x8)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ SECONDPATH (0x2)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

**變更 \_ LOG \_ ENTRYFLAGS \_ SHORTNAME (0x10)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ TEMPPATH (0x1)**
</dt> </dl> </dd> <dt>

**dwAttributes**
</dt> <dd>

變更記錄檔的檔案屬性。 如果未指定任何屬性，此值應該設定為0xFFFFFFFF。

</dd> <dt>

**i64SequenceNum**
</dt> <dd>

指派給變更記錄專案的序號。

</dd> <dt>

**szProcName**
</dt> <dd>

進行變更之進程的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

此結構後面會加上可變長度資料記錄的可變長度，加上與 **RecordHeader** 的 **dwRecordSize** 成員值相同的 **DWORD** 值。

可變長度的資料記錄是由 [**記錄 \_ 標頭**](record-header.md) 結構加上可用來還原變更記錄專案的資料所組成。 資料的格式取決於 **記錄 \_ 標頭** 結構之 **dwRecordType** 成員的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                            |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                       |



 

 





