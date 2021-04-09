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
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024738"
---
# <a name="change_log_entry-structure"></a><span data-ttu-id="be45e-105">變更 \_ 記錄 \_ 專案結構</span><span class="sxs-lookup"><span data-stu-id="be45e-105">CHANGE\_LOG\_ENTRY structure</span></span>

<span data-ttu-id="be45e-106">\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]</span><span class="sxs-lookup"><span data-stu-id="be45e-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="be45e-107">變更記錄專案。</span><span class="sxs-lookup"><span data-stu-id="be45e-107">A change log entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="be45e-108">語法</span><span class="sxs-lookup"><span data-stu-id="be45e-108">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="be45e-109">成員</span><span class="sxs-lookup"><span data-stu-id="be45e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="be45e-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="be45e-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-111">[**記錄 \_ 標頭**](record-header.md)結構。</span><span class="sxs-lookup"><span data-stu-id="be45e-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="be45e-112">**DwRecordType** 成員應設定為 **RecordTypeLogEntry** (1) 。</span><span class="sxs-lookup"><span data-stu-id="be45e-112">The **dwRecordType** member should be set to **RecordTypeLogEntry** (1).</span></span>

</dd> <dt>

<span data-ttu-id="be45e-113">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="be45e-113">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-114">此成員應設定為0xabcdef12。</span><span class="sxs-lookup"><span data-stu-id="be45e-114">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="be45e-115">**dwEntryType**</span><span class="sxs-lookup"><span data-stu-id="be45e-115">**dwEntryType**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-116">這個成員可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="be45e-116">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

<span data-ttu-id="be45e-117">CHANGE \_ LOG \_ ENTRYTYPES \_ ACLCHANGE \* \* (0x2) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-117">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ACLCHANGE\*\* (0x2)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

<span data-ttu-id="be45e-118">CHANGE \_ LOG \_ ENTRYTYPES \_ ATTRCHANGE \* \* (0x4) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-118">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ATTRCHANGE\*\* (0x4)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

<span data-ttu-id="be45e-119">CHANGE \_ LOG \_ ENTRYTYPES \_ DIRCREATE \* \* (0x80) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-119">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRCREATE\*\* (0x80)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

<span data-ttu-id="be45e-120">CHANGE \_ LOG \_ ENTRYTYPES \_ DIRRENAME \* \* (0x100) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-120">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRRENAME\*\* (0x100)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

<span data-ttu-id="be45e-121">CHANGE \_ LOG \_ ENTRYTYPES \_ DIRDELETE \* \* (0x200) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-121">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRDELETE\*\* (0x200)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

<span data-ttu-id="be45e-122">CHANGE \_ LOG \_ ENTRYTYPES \_ FILECREATE \* \* (0x20) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-122">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILECREATE\*\* (0x20)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

<span data-ttu-id="be45e-123">CHANGE \_ LOG \_ ENTRYTYPES \_ FILEDELETE \* \* (0x10) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-123">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILEDELETE\*\* (0x10)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

<span data-ttu-id="be45e-124">CHANGE \_ LOG \_ ENTRYTYPES \_ FILERENAME \* \* (0x40) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-124">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILERENAME\*\* (0x40)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

<span data-ttu-id="be45e-125">CHANGE \_ LOG \_ ENTRYTYPES \_ INPRECREATE \* \* (0x100000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-125">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_INPRECREATE\*\* (0x100000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

<span data-ttu-id="be45e-126">CHANGE \_ LOG \_ ENTRYTYPES \_ ISDIR \* \* (0x20000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-126">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISDIR\*\* (0x20000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

<span data-ttu-id="be45e-127">CHANGE \_ LOG \_ ENTRYTYPES \_ ISNOTDIR \* \* (0x40000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-127">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISNOTDIR\*\* (0x40000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

<span data-ttu-id="be45e-128">CHANGE \_ LOG \_ ENTRYTYPES \_ MOUNTCREATE \* \* (0x400) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-128">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTCREATE\*\* (0x400)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

<span data-ttu-id="be45e-129">CHANGE \_ LOG \_ ENTRYTYPES \_ MOUNTDELETE \* \* (0x800) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-129">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTDELETE\*\* (0x800)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

<span data-ttu-id="be45e-130">CHANGE \_ LOG \_ ENTRYTYPES \_ NOOPTIMIZE \* \* (0x10000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-130">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_NOOPTIMIZE\*\* (0x10000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

<span data-ttu-id="be45e-131">CHANGE \_ LOG \_ ENTRYTYPES \_ OPENBYID \* \* (0x200000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-131">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_OPENBYID\*\* (0x200000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

<span data-ttu-id="be45e-132">CHANGE \_ LOG \_ ENTRYTYPES \_ SIMULATEDELETE \* \* (0x80000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-132">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_SIMULATEDELETE\*\* (0x80000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

<span data-ttu-id="be45e-133">CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMCHANGE \* \* (0x1) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-133">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCHANGE\*\* (0x1)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

<span data-ttu-id="be45e-134">CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMCREATE \* \* (0x2000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-134">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCREATE\*\* (0x2000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

<span data-ttu-id="be45e-135">CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMOVERWRITE \* \* (0x8) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-135">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMOVERWRITE\*\* (0x8)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

<span data-ttu-id="be45e-136">CHANGE \_ LOG \_ ENTRYTYPES \_ VOLUMEERROR \* \* (0x1000) \* \*</span><span class="sxs-lookup"><span data-stu-id="be45e-136">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_VOLUMEERROR\*\* (0x1000)\*\*</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="be45e-137">**dwEntryFlags**</span><span class="sxs-lookup"><span data-stu-id="be45e-137">**dwEntryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-138">這個成員可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="be45e-138">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

<span data-ttu-id="be45e-139">**CHANGE \_ LOG \_ ENTRYFLAGS \_ ACLINFO (0x4)**</span><span class="sxs-lookup"><span data-stu-id="be45e-139">**CHANGE\_LOG\_ENTRYFLAGS\_ACLINFO (0x4)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

<span data-ttu-id="be45e-140">**CHANGE \_ LOG \_ ENTRYFLAGS \_ DEBUGINFO (0x8)**</span><span class="sxs-lookup"><span data-stu-id="be45e-140">**CHANGE\_LOG\_ENTRYFLAGS\_DEBUGINFO (0x8)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

<span data-ttu-id="be45e-141">**CHANGE \_ LOG \_ ENTRYFLAGS \_ SECONDPATH (0x2)**</span><span class="sxs-lookup"><span data-stu-id="be45e-141">**CHANGE\_LOG\_ENTRYFLAGS\_SECONDPATH (0x2)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

<span data-ttu-id="be45e-142">**變更 \_ LOG \_ ENTRYFLAGS \_ SHORTNAME (0x10)**</span><span class="sxs-lookup"><span data-stu-id="be45e-142">**CHANGE\_LOG\_ENTRYFLAGS\_SHORTNAME (0x10)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

<span data-ttu-id="be45e-143">**CHANGE \_ LOG \_ ENTRYFLAGS \_ TEMPPATH (0x1)**</span><span class="sxs-lookup"><span data-stu-id="be45e-143">**CHANGE\_LOG\_ENTRYFLAGS\_TEMPPATH (0x1)**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="be45e-144">**dwAttributes**</span><span class="sxs-lookup"><span data-stu-id="be45e-144">**dwAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-145">變更記錄檔的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="be45e-145">The file attributes of the change log file.</span></span> <span data-ttu-id="be45e-146">如果未指定任何屬性，此值應該設定為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="be45e-146">If no attributes are specified, this value should be set to 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="be45e-147">**i64SequenceNum**</span><span class="sxs-lookup"><span data-stu-id="be45e-147">**i64SequenceNum**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-148">指派給變更記錄專案的序號。</span><span class="sxs-lookup"><span data-stu-id="be45e-148">The sequence number assigned to the change log entry.</span></span>

</dd> <dt>

<span data-ttu-id="be45e-149">**szProcName**</span><span class="sxs-lookup"><span data-stu-id="be45e-149">**szProcName**</span></span>
</dt> <dd>

<span data-ttu-id="be45e-150">進行變更之進程的名稱。</span><span class="sxs-lookup"><span data-stu-id="be45e-150">The name of the process making the change.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be45e-151">備註</span><span class="sxs-lookup"><span data-stu-id="be45e-151">Remarks</span></span>

<span data-ttu-id="be45e-152">此結構後面會加上可變長度資料記錄的可變長度，加上與 **RecordHeader** 的 **dwRecordSize** 成員值相同的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="be45e-152">This structure is followed by a variable number of variable-length data records, plus a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

<span data-ttu-id="be45e-153">可變長度的資料記錄是由 [**記錄 \_ 標頭**](record-header.md) 結構加上可用來還原變更記錄專案的資料所組成。</span><span class="sxs-lookup"><span data-stu-id="be45e-153">The variable-length data records consist of a [**RECORD\_HEADER**](record-header.md) structure plus data that can be used to restore the change log entry.</span></span> <span data-ttu-id="be45e-154">資料的格式取決於 **記錄 \_ 標頭** 結構之 **dwRecordType** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="be45e-154">The format of the data depends on the value of the **dwRecordType** member of the **RECORD\_HEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="be45e-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="be45e-155">Requirements</span></span>



| <span data-ttu-id="be45e-156">需求</span><span class="sxs-lookup"><span data-stu-id="be45e-156">Requirement</span></span> | <span data-ttu-id="be45e-157">值</span><span class="sxs-lookup"><span data-stu-id="be45e-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be45e-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be45e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="be45e-159">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be45e-159">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="be45e-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be45e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="be45e-161">都不支援</span><span class="sxs-lookup"><span data-stu-id="be45e-161">None supported</span></span><br/>                            |
| <span data-ttu-id="be45e-162">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="be45e-162">End of client support</span></span><br/>    | <span data-ttu-id="be45e-163">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="be45e-163">Windows XP with SP2</span></span><br/>                       |



 

 





