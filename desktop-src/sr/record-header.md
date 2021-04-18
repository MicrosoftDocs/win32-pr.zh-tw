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
# <a name="record_header-structure"></a><span data-ttu-id="4326c-105">記錄 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="4326c-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="4326c-106">\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]</span><span class="sxs-lookup"><span data-stu-id="4326c-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="4326c-107">[**變更記錄 \_ \_ 專案**](change-log-entry.md)所使用的記錄標頭，以及 [**變更記錄 \_ \_ 標頭**](change-log-header.md)結構。</span><span class="sxs-lookup"><span data-stu-id="4326c-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="4326c-108">語法</span><span class="sxs-lookup"><span data-stu-id="4326c-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="4326c-109">成員</span><span class="sxs-lookup"><span data-stu-id="4326c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4326c-110">**dwRecordSize**</span><span class="sxs-lookup"><span data-stu-id="4326c-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="4326c-111">記錄的總大小，包括標頭（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4326c-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4326c-112">**dwRecordType**</span><span class="sxs-lookup"><span data-stu-id="4326c-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="4326c-113">記錄類型。</span><span class="sxs-lookup"><span data-stu-id="4326c-113">The record type.</span></span> <span data-ttu-id="4326c-114">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4326c-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="4326c-115">值</span><span class="sxs-lookup"><span data-stu-id="4326c-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="4326c-116">意義</span><span class="sxs-lookup"><span data-stu-id="4326c-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="4326c-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="4326c-118">記錄是變更記錄的標頭。</span><span class="sxs-lookup"><span data-stu-id="4326c-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="4326c-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="4326c-120">記錄是變更記錄專案的標頭。</span><span class="sxs-lookup"><span data-stu-id="4326c-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="4326c-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="4326c-122">資料是變更記錄專案的磁片區路徑。</span><span class="sxs-lookup"><span data-stu-id="4326c-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="4326c-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="4326c-124">資料是變更記錄專案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="4326c-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="4326c-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="4326c-126">重新命名變更記錄檔專案時，會使用資料。此路徑是重新命名檔案的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="4326c-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="4326c-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="4326c-128">資料是用來還原變更記錄專案的備份檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="4326c-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="4326c-129">備份檔案位於 RP *n* 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="4326c-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="4326c-130">檔案名的格式如下：*>xxxxxxx*。*ext*，其中 *>xxxxxxx* 是七位數的數位，而 *ext* 是副檔名。</span><span class="sxs-lookup"><span data-stu-id="4326c-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="4326c-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="4326c-132">資料是 ACL。</span><span class="sxs-lookup"><span data-stu-id="4326c-132">The data is an ACL.</span></span> <span data-ttu-id="4326c-133">資料格式是 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構。</span><span class="sxs-lookup"><span data-stu-id="4326c-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="4326c-134">此值不能大於8192個位元組。</span><span class="sxs-lookup"><span data-stu-id="4326c-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="4326c-135">若要指定大於8192個位元組的值，請使用 **RecordTypeAclFile** 成員。</span><span class="sxs-lookup"><span data-stu-id="4326c-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="4326c-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="4326c-137">資料是用來儲存 ACL 的 ACL 檔案名。</span><span class="sxs-lookup"><span data-stu-id="4326c-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="4326c-138">ACL 檔案位於 RP *n* 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="4326c-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="4326c-139">檔案名的格式如下： S *>xxxxxxx*，其中 *>xxxxxxx* 是七位數的數位。</span><span class="sxs-lookup"><span data-stu-id="4326c-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="4326c-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="4326c-141">資料是變更記錄專案的偵錯工具資訊。</span><span class="sxs-lookup"><span data-stu-id="4326c-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="4326c-142">資料格式為 **SR 記錄檔 \_ 的 \_ DEBUG \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="4326c-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="4326c-143">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4326c-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="4326c-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4326c-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="4326c-145">資料是備份檔案的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="4326c-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4326c-146">備註</span><span class="sxs-lookup"><span data-stu-id="4326c-146">Remarks</span></span>

<span data-ttu-id="4326c-147">**SR \_ 記錄檔 \_ DEBUG \_ 資訊** 結構的定義如下。</span><span class="sxs-lookup"><span data-stu-id="4326c-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="4326c-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="4326c-148">Requirements</span></span>



| <span data-ttu-id="4326c-149">需求</span><span class="sxs-lookup"><span data-stu-id="4326c-149">Requirement</span></span> | <span data-ttu-id="4326c-150">值</span><span class="sxs-lookup"><span data-stu-id="4326c-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4326c-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4326c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4326c-152">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4326c-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4326c-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4326c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4326c-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="4326c-154">None supported</span></span><br/>                            |
| <span data-ttu-id="4326c-155">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4326c-155">End of client support</span></span><br/>    | <span data-ttu-id="4326c-156">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="4326c-156">Windows XP with SP2</span></span><br/>                       |



 

