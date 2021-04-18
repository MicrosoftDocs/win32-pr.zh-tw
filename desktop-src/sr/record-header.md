---
title: RECORD_HEADER 結構
description: 變更記錄專案所使用的記錄標頭 \_ \_ ，以及變更記錄 \_ \_ 標頭結構。
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- RECORD_HEADER 結構系統還原
- PRECORD_HEADER 結構指標系統還原
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466357"
---
# <a name="record_header-structure"></a>記錄 \_ 標頭結構

\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]

[**變更記錄 \_ \_ 專案**](change-log-entry.md)所使用的記錄標頭，以及 [**變更記錄 \_ \_ 標頭**](change-log-header.md)結構。

## <a name="syntax"></a>語法


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**dwRecordSize**
</dt> <dd>

記錄的總大小，包括標頭（以位元組為單位）。

</dd> <dt>

**dwRecordType**
</dt> <dd>

記錄類型。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**RecordTypeLogHeader**</dt> <dt>0</dt> </dl>     | 記錄是變更記錄的標頭。<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**RecordTypeLogEntry**</dt> <dt>1</dt> </dl>         | 記錄是變更記錄專案的標頭。<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**RecordTypeVolumePath**</dt> <dt>2</dt> </dl> | 資料是變更記錄專案的磁片區路徑。<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**RecordTypeFirstPath**</dt> <dt>3</dt> </dl>     | 資料是變更記錄專案的檔案路徑。<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**RecordTypeSecondPath**</dt> <dt>4</dt> </dl> | 重新命名變更記錄檔專案時，會使用資料。此路徑是重新命名檔案的儲存位置。<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**RecordTypeTempPath**</dt> <dt>5</dt> </dl>         | 資料是用來還原變更記錄專案的備份檔案名稱。 備份檔案位於 RP *n* 資料夾中。 檔案名的格式如下：*>xxxxxxx*。*ext*，其中 *>xxxxxxx* 是七位數的數位，而 *ext* 是副檔名。<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**RecordTypeAclInline**</dt> <dt>6</dt> </dl>     | 資料是 ACL。 資料格式是 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構。 <br/> 此值不能大於8192個位元組。 若要指定大於8192個位元組的值，請使用 **RecordTypeAclFile** 成員。<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**RecordTypeAclFile**</dt> <dt>7</dt> </dl>             | 資料是用來儲存 ACL 的 ACL 檔案名。 ACL 檔案位於 RP *n* 資料夾中。 檔案名的格式如下： S *>xxxxxxx*，其中 *>xxxxxxx* 是七位數的數位。<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**RecordTypeDebugInfo**</dt> <dt>8</dt> </dl>     | 資料是變更記錄專案的偵錯工具資訊。 資料格式為 **SR 記錄檔 \_ 的 \_ DEBUG \_ 資訊** 結構。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**RecordTypeShortName**</dt> <dt>9</dt> </dl>     | 資料是備份檔案的簡短名稱。<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>備註

**SR \_ 記錄檔 \_ DEBUG \_ 資訊** 結構的定義如下。

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                            |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                       |



 

