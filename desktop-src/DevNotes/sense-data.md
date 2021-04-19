---
description: 用來報告狀態或錯誤資訊，以回應 SCSI 要求感知命令。
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: 'SENSE_DATA 結構 (Scsi-3) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106988536"
---
# <a name="sense_data-structure"></a><span data-ttu-id="eeb54-103">意義 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="eeb54-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="eeb54-104">用來報告狀態或錯誤資訊，以回應 SCSI **要求感知** 命令。</span><span class="sxs-lookup"><span data-stu-id="eeb54-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb54-105">語法</span><span class="sxs-lookup"><span data-stu-id="eeb54-105">Syntax</span></span>


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a><span data-ttu-id="eeb54-106">成員</span><span class="sxs-lookup"><span data-stu-id="eeb54-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eeb54-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eeb54-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-108">報表類型。</span><span class="sxs-lookup"><span data-stu-id="eeb54-108">The report type.</span></span>



| <span data-ttu-id="eeb54-109">值</span><span class="sxs-lookup"><span data-stu-id="eeb54-109">Value</span></span>                                                                           | <span data-ttu-id="eeb54-110">意義</span><span class="sxs-lookup"><span data-stu-id="eeb54-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="eeb54-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="eeb54-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="eeb54-112">目前的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eeb54-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="eeb54-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="eeb54-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="eeb54-114">延遲的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eeb54-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eeb54-115">**有效**</span><span class="sxs-lookup"><span data-stu-id="eeb54-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-116">如果 **資訊** 欄位定義于標準中，則為1。否則， **資訊** 欄位是廠商專屬的，而且不是由標準所定義。</span><span class="sxs-lookup"><span data-stu-id="eeb54-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-117">**SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="eeb54-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-118">已過時。</span><span class="sxs-lookup"><span data-stu-id="eeb54-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-119">**SenseKey**</span><span class="sxs-lookup"><span data-stu-id="eeb54-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-120">指出錯誤的類別。</span><span class="sxs-lookup"><span data-stu-id="eeb54-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="eeb54-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**沒有意義** (0x0) </span><span class="sxs-lookup"><span data-stu-id="eeb54-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**復原的錯誤** (0x1) </span><span class="sxs-lookup"><span data-stu-id="eeb54-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (0x2) </span><span class="sxs-lookup"><span data-stu-id="eeb54-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**中度錯誤** (0x3) </span><span class="sxs-lookup"><span data-stu-id="eeb54-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**硬體錯誤** (0x4) </span><span class="sxs-lookup"><span data-stu-id="eeb54-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>不 **合法的要求** (0x5) </span><span class="sxs-lookup"><span data-stu-id="eeb54-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span> (0x6) 的 **單元注意**</span><span class="sxs-lookup"><span data-stu-id="eeb54-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**資料保護** (0x7) </span><span class="sxs-lookup"><span data-stu-id="eeb54-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span> (0x9) 的 **固件錯誤**</span><span class="sxs-lookup"><span data-stu-id="eeb54-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**中止的命令** (0xB) </span><span class="sxs-lookup"><span data-stu-id="eeb54-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**等於** (0xC) </span><span class="sxs-lookup"><span data-stu-id="eeb54-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span> (0xD) 的 **磁片區溢** 位</span><span class="sxs-lookup"><span data-stu-id="eeb54-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="eeb54-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE) </span><span class="sxs-lookup"><span data-stu-id="eeb54-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="eeb54-134">**已保留**</span><span class="sxs-lookup"><span data-stu-id="eeb54-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-135">保留的。</span><span class="sxs-lookup"><span data-stu-id="eeb54-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-136">**IncorrectLength**</span><span class="sxs-lookup"><span data-stu-id="eeb54-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-137">1，如果要求的邏輯區塊長度不符合媒體上資料的邏輯區塊長度。</span><span class="sxs-lookup"><span data-stu-id="eeb54-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-138">**EndOfMedia**</span><span class="sxs-lookup"><span data-stu-id="eeb54-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-139">1，如果連續存取裝置已到達媒體的結尾，或印表機已缺紙。</span><span class="sxs-lookup"><span data-stu-id="eeb54-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-140">**尚未調准**</span><span class="sxs-lookup"><span data-stu-id="eeb54-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-141">如果目前的命令已到達標記或 setmark，則為1。</span><span class="sxs-lookup"><span data-stu-id="eeb54-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="eeb54-142">僅適用于順序存取裝置。</span><span class="sxs-lookup"><span data-stu-id="eeb54-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-143">**資訊**</span><span class="sxs-lookup"><span data-stu-id="eeb54-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-144">裝置類型或命令特有的資料。</span><span class="sxs-lookup"><span data-stu-id="eeb54-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-145">**AdditionalSenseLength**</span><span class="sxs-lookup"><span data-stu-id="eeb54-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-146">結構其餘部分的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eeb54-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="eeb54-147">總長度減去7。</span><span class="sxs-lookup"><span data-stu-id="eeb54-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-148">**CommandSpecificInformation**</span><span class="sxs-lookup"><span data-stu-id="eeb54-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-149">命令特有的資料。</span><span class="sxs-lookup"><span data-stu-id="eeb54-149">Command-specific data.</span></span> <span data-ttu-id="eeb54-150">值是在適當的命令標準中定義。</span><span class="sxs-lookup"><span data-stu-id="eeb54-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-151">**AdditionalSenseCode**</span><span class="sxs-lookup"><span data-stu-id="eeb54-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-152">描述 **SenseKey** 欄位中所報告之錯誤的裝置特定程式碼。</span><span class="sxs-lookup"><span data-stu-id="eeb54-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-153">**AdditionalSenseCodeQualifier**</span><span class="sxs-lookup"><span data-stu-id="eeb54-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-154">可以包含 **AdditionalSenseCode** 欄位的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eeb54-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-155">**FieldReplaceableUnitCode**</span><span class="sxs-lookup"><span data-stu-id="eeb54-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-156">與此意義資料相關聯之元件的 Vender 特定資訊。</span><span class="sxs-lookup"><span data-stu-id="eeb54-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="eeb54-157">**SenseKeySpecific**</span><span class="sxs-lookup"><span data-stu-id="eeb54-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="eeb54-158">意義重要的特定資訊的內容和格式是由 **SenseKey** 欄位的值所決定。</span><span class="sxs-lookup"><span data-stu-id="eeb54-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeb54-159">備註</span><span class="sxs-lookup"><span data-stu-id="eeb54-159">Remarks</span></span>

<span data-ttu-id="eeb54-160">如需有關意義資料格式的詳細資訊，請參閱 [SCSI 要求感知命令](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command) 。</span><span class="sxs-lookup"><span data-stu-id="eeb54-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb54-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeb54-161">Requirements</span></span>



| <span data-ttu-id="eeb54-162">需求</span><span class="sxs-lookup"><span data-stu-id="eeb54-162">Requirement</span></span> | <span data-ttu-id="eeb54-163">值</span><span class="sxs-lookup"><span data-stu-id="eeb54-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="eeb54-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeb54-164">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb54-165">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeb54-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eeb54-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeb54-166">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb54-167">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeb54-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eeb54-168">標頭</span><span class="sxs-lookup"><span data-stu-id="eeb54-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeb54-169"><dt>Scsi。h</dt></span><span class="sxs-lookup"><span data-stu-id="eeb54-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb54-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeb54-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb54-171">iSCSI 目標傳遞</span><span class="sxs-lookup"><span data-stu-id="eeb54-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="eeb54-172">SCSI \_ \_ 通過 \_ DIRECT</span><span class="sxs-lookup"><span data-stu-id="eeb54-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




