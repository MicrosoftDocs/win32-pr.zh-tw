---
title: 'IMAPI.EXE 傳回值 (Imapi2error) '
description: IMAPI.EXE 方法會傳回非負數值， (通常會 \_ 在方法成功時) 正常。 當失敗時，IMAPI.EXE 方法會傳回 Winerror.h .h、Imapi2error 或 Imapi2fserror 的成功或錯誤碼。
ms.assetid: 0e62ed6c-4810-4d36-a759-9b02b68face6
topic_type:
- apiref
api_name:
- E_IMAPI_BURN_VERIFICATION_FAILED
- E_IMAPI_REQUEST_CANCELLED
- E_IMAPI_RECORDER_REQUIRED
- S_IMAPI_WRITE_NOT_IN_PROGRESS
- S_IMAPI_SPEEDADJUSTED
- S_IMAPI_ROTATIONADJUSTED
- S_IMAPI_BOTHADJUSTED
- S_IMAPI_COMMAND_HAS_SENSE_DATA
- E_IMAPI_RAW_IMAGE_IS_READ_ONLY
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS
- E_IMAPI_RAW_IMAGE_NO_TRACKS
- E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED
- E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED
- E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND
- S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX
- E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE
- E_IMAPI_RECORDER_MEDIA_NO_MEDIA
- E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE
- E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN
- E_IMAPI_RECORDER_MEDIA_BECOMING_READY
- E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS
- E_IMAPI_RECORDER_MEDIA_BUSY
- E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS
- E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED
- E_IMAPI_RECORDER_NO_SUCH_FEATURE
- E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT
- E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED
- E_IMAPI_RECORDER_COMMAND_TIMEOUT
- E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT
- E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH
- E_IMAPI_RECORDER_LOCKED
- E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE
- E_IMAPI_LOSS_OF_STREAMING
- E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE
- E_IMAPI_DF2DATA_WRITE_IN_PROGRESS
- E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2DATA_INVALID_MEDIA_STATE
- E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA
- E_IMAPI_DF2DATA_MEDIA_NOT_BLANK
- E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2TAO_WRITE_IN_PROGRESS
- E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2TAO_MEDIA_IS_PREPARED
- E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY
- E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED
- E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE
- E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2TAO_INVALID_ISRC
- E_IMAPI_DF2TAO_INVALID_MCN
- E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_WRITE_IN_PROGRESS
- E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2RAW_MEDIA_IS_PREPARED
- E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE
- E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED
- E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT
- E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_IN_USE
- E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED
- E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL
- E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL
- E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE
- E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND
- E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR
- E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE
- E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND
- E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID
- IMAPI_E_FSI_INTERNAL_ERROR
- IMAPI_E_INVALID_PARAM
- IMAPI_E_READONLY
- IMAPI_E_NO_OUTPUT
- IMAPI_E_INVALID_VOLUME_NAME
- IMAPI_E_INVALID_DATE
- IMAPI_E_FILE_SYSTEM_NOT_EMPTY
- IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED
- IMAPI_E_NOT_FILE
- IMAPI_E_NOT_DIR
- IMAPI_E_DIR_NOT_EMPTY
- IMAPI_E_NOT_IN_FILE_SYSTEM
- IMAPI_E_INVALID_PATH
- IMAPI_E_RESTRICTED_NAME_VIOLATION
- IMAPI_E_DUP_NAME
- IMAPI_E_NO_UNIQUE_NAME
- IMAPI_E_ITEM_NOT_FOUND
- IMAPI_E_FILE_NOT_FOUND
- IMAPI_E_DIR_NOT_FOUND
- IMAPI_E_IMAGE_SIZE_LIMIT
- IMAPI_E_IMAGE_TOO_BIG
- IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED
- IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND
- IMAPI_E_IMAGEMANAGER_NO_IMAGE
- IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG
- IMAPI_E_DATA_STREAM_INCONSISTENCY
- IMAPI_E_DATA_STREAM_READ_FAILURE
- IMAPI_E_DATA_STREAM_CREATE_FAILURE
- IMAPI_E_DIRECTORY_READ_FAILURE
- IMAPI_E_TOO_MANY_DIRS
- IMAPI_E_ISO9660_LEVELS
- IMAPI_E_DATA_TOO_BIG
- IMAPI_E_STASHFILE_OPEN_FAILURE
- IMAPI_E_STASHFILE_SEEK_FAILURE
- IMAPI_E_STASHFILE_WRITE_FAILURE
- IMAPI_E_STASHFILE_READ_FAILURE
- IMAPI_E_INVALID_WORKING_DIRECTORY
- IMAPI_E_WORKING_DIRECTORY_SPACE
- IMAPI_E_STASHFILE_MOVE
- IMAPI_E_BOOT_IMAGE_DATA
- IMAPI_E_BOOT_OBJECT_CONFLICT
- IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH
- IMAPI_E_EMPTY_DISC
- IMAPI_E_NO_SUPPORTED_FILE_SYSTEM
- IMAPI_E_FILE_SYSTEM_NOT_FOUND
- IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR
- IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED
- IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY
- IMAPI_E_IMPORT_SEEK_FAILURE
- IMAPI_E_IMPORT_READ_FAILURE
- IMAPI_E_DISC_MISMATCH
- IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED
- IMAPI_E_UDF_NOT_WRITE_COMPATIBLE
- IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION
- IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_MULTISESSION_NOT_SET
- IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE
- IMAPI_E_BAD_MULTISESSION_PARAMETER
- IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED
api_location:
- Imapi2error.h
- Imapi2fserror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bc4b99bb5ac123ea26ca1deb755fa29598811b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465604"
---
# <a name="imapi-return-values"></a><span data-ttu-id="c9b4e-104">IMAPI.EXE 傳回值</span><span class="sxs-lookup"><span data-stu-id="c9b4e-104">IMAPI Return Values</span></span>

<span data-ttu-id="c9b4e-105">IMAPI.EXE 方法會傳回非負數值， (通常會 \_ 在方法成功時) 正常。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-105">The IMAPI methods return non-negative values, (typically S\_OK) if the method was successful.</span></span> <span data-ttu-id="c9b4e-106">當失敗時，IMAPI.EXE 方法會傳回 Winerror.h .h、Imapi2error 或 Imapi2fserror 的成功或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-106">The IMAPI methods return success or error codes from Winerror.h, Imapi2error.h, or Imapi2fserror.h, on failure.</span></span>

<span data-ttu-id="c9b4e-107">已定義下列成功和錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-107">The following success and error codes are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c9b4e-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="c9b4e-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c9b4e-109">Description</span><span class="sxs-lookup"><span data-stu-id="c9b4e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl> <span data-ttu-id="c9b4e-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt> (HRESULT) 0xC0AA0007L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT)0xC0AA0007L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-111">光碟未通過燒錄驗證，可能包含損毀的資料或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-111">The disc did not pass burn verification and may contain corrupt data or be unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl> <span data-ttu-id="c9b4e-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt> (HRESULT) 0xC0AA0002</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT)0xC0AA0002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-113">已取消要求。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-113">The request was canceled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl> <span data-ttu-id="c9b4e-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt> (HRESULT) 0xC0AA0003</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT)0xC0AA0003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-115">要求必須選取目前的光碟錄製器。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-115">The request requires a current disc recorder to be selected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl> <span data-ttu-id="c9b4e-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0x00AA0302L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0x00AA0302L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-117">目前沒有任何寫入作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-117">No write operation is currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl> <span data-ttu-id="c9b4e-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt> (HRESULT) 0x00AA0004</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-119">磁片磁碟機不支援要求的寫入速度，並且已調整速度。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-119">The requested write speed was not supported by the drive and the speed was adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl> <span data-ttu-id="c9b4e-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt> (HRESULT) 0x00AA0005</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-121">磁片磁碟機不支援要求的旋轉類型，且已調整旋轉類型。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-121">The requested rotation type was not supported by the drive and the rotation type was adjusted.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl> <span data-ttu-id="c9b4e-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt> (HRESULT) 0x00AA0006</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0006</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-123">磁片磁碟機不支援要求的寫入速度和旋轉類型，而且兩者都經過調整。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-123">The requested write speed and rotation type were not supported by the drive and they were both adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl> <span data-ttu-id="c9b4e-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt> (HRESULT) 0x00AA0200</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT)0x00AA0200</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-125">裝置已接受命令，但傳回的意義資料表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-125">The device accepted the command, but returned sense data, indicating an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl> <span data-ttu-id="c9b4e-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt> (HRESULT) 0x80AA0A00L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT)0x80AA0A00L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-127">因為呼叫 <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator：： CreateResultImage</strong></a>，所以映射已變成隻讀。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-127">The image has become read-only due to a call to <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>.</span></span> <span data-ttu-id="c9b4e-128">因此無法再修改物件。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-128">As a result the object can no longer be modified.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl> <span data-ttu-id="c9b4e-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt> (HRESULT) 0x80AA0A01L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A01L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-130">可能不會再新增任何曲目。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-130">No more tracks may be added.</span></span> <span data-ttu-id="c9b4e-131">CD 媒體的範圍限制為1-99 個曲目。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-131">CD media is restricted to a range of 1-99 tracks.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl> <span data-ttu-id="c9b4e-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt> (HRESULT) 0x80AA0A03L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A03L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-133">使用此函式之前，必須先將追蹤新增至影像。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-133">Tracks must be added to the image before using this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl> <span data-ttu-id="c9b4e-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0x80AA0A02L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0A02L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-135">不支援要求的磁區類型。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-135">The requested sector type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl> <span data-ttu-id="c9b4e-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt> (HRESULT) 0x80AA0A04L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT)0x80AA0A04L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-137">使用此函式之前，可能不會將追蹤新增至影像。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-137">Tracks may not be added to the image prior to the use of this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl> <span data-ttu-id="c9b4e-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt> (HRESULT) 0x80AA0A05L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT)0x80AA0A05L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-139">新增此播放軌會超過 leadout 開頭的限制。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-139">Adding this track would exceed the limitations of the start of the leadout.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl> <span data-ttu-id="c9b4e-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt> (HRESULT) 0x80AA0A06L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT)0x80AA0A06L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-141">新增此播放軌會超過99索引限制。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-141">Adding this track would exceed the 99 index limit.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl> <span data-ttu-id="c9b4e-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt> (HRESULT) 0x80AA0A07L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT)0x80AA0A07L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-143">指定的 LBA 位移不在追蹤索引的清單中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-143">The specified LBA offset is not in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl> <span data-ttu-id="c9b4e-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt> (HRESULT) 0x00AA0A08L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT)0x00AA0A08L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-145">指定的 LBA 位移已經在追蹤索引的清單中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-145">The specified LBA offset is already in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl> <span data-ttu-id="c9b4e-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt> (HRESULT) 0x80AA0A09L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT)0x80AA0A09L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-147">無法清除索引 1 (LBA offset 0) 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-147">Index 1 (LBA offset zero) cannot be cleared.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl> <span data-ttu-id="c9b4e-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt> (HRESULT) 0x80AA0A0AL</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT)0x80AA0A0AL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-149">每個索引都必須有10個磁區的最小大小。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-149">Each index must have a minimum size of ten sectors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl> <span data-ttu-id="c9b4e-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt> (HRESULT) 0xC0AA0201</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT)0xC0AA0201</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-151">裝置回報要求的模式頁面 (，且類型) 不存在。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-151">The device reported that the requested mode page (and type) is not present.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl> <span data-ttu-id="c9b4e-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt> (HRESULT) 0xC0AA0202</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0202</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-153">裝置中沒有任何媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-153">There is no media in the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl> <span data-ttu-id="c9b4e-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt> (HRESULT) 0xC0AA0203</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AA0203</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-155">媒體與未知的實體格式不相容。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-155">The media is not compatible or of unknown physical format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl> <span data-ttu-id="c9b4e-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt> (HRESULT) 0xC0AA0204</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT)0xC0AA0204</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-157">媒體會朝下插入。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-157">The media is inserted upside down.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl> <span data-ttu-id="c9b4e-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt> (HRESULT) 0xC0AA0205</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT)0xC0AA0205</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-159">磁片磁碟機回報正在準備就緒。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-159">The drive reported that it is in the process of becoming ready.</span></span> <span data-ttu-id="c9b4e-160">請稍後再試一次要求。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-160">Please try the request again later.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl> <span data-ttu-id="c9b4e-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0206</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0206</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-162">媒體目前正在格式化。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-162">The media is currently being formatted.</span></span> <span data-ttu-id="c9b4e-163">請等候格式完成，再嘗試使用媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-163">Please wait for the format to complete before attempting to use the media.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl> <span data-ttu-id="c9b4e-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt> (HRESULT) 0xC0AA0207</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT)0xC0AA0207</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-165">磁片磁碟機回報它正在執行長時間執行的作業，例如完成寫入。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-165">The drive reported that it is performing a long-running operation, such as finishing a write.</span></span> <span data-ttu-id="c9b4e-166">磁片磁碟機可能很長一段時間無法使用。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-166">The drive may be unusable for a long period of time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl> <span data-ttu-id="c9b4e-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt> (HRESULT) 0xC0AA0208</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT)0xC0AA0208</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-168">磁片磁碟機回報，不支援在模式選取命令的模式頁面中提供的參數組合。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-168">The drive reported that the combination of parameters provided in the mode page for a MODE SELECT command were not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl> <span data-ttu-id="c9b4e-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt> (HRESULT) 0xC0AA0209</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT)0xC0AA0209</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-170">磁片磁碟機報告媒體已受寫入保護。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-170">The drive reported that the media is write protected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl> <span data-ttu-id="c9b4e-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt> (HRESULT) 0xC0AA020A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT)0xC0AA020A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-172">裝置不支援要求的功能頁面。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-172">The feature page requested is not supported by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl> <span data-ttu-id="c9b4e-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt> (HRESULT) 0xC0AA020B</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT)0xC0AA020B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-174">支援要求的功能頁面，但未標示為最新。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-174">The feature page requested is supported, but is not marked as current.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl> <span data-ttu-id="c9b4e-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA020C</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA020C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-176">磁片磁碟機不支援 GET CONFIGURATION 命令。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-176">The drive does not support the GET CONFIGURATION command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl> <span data-ttu-id="c9b4e-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt> (HRESULT) 0xC0AA020D</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT)0xC0AA020D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-178">裝置無法接受超時時間內的命令。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-178">The device failed to accept the command within the timeout period.</span></span> <span data-ttu-id="c9b4e-179">這可能是因為裝置進入不一致的狀態，或命令的超時值可能需要增加。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-179">This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl> <span data-ttu-id="c9b4e-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt> (HRESULT) 0xC0AA020E</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT)0xC0AA020E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-181">DVD 結構不存在。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-181">The DVD structure is not present.</span></span> <span data-ttu-id="c9b4e-182">這可能是因為使用的驅動程式/媒體不相容所造成。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-182">This may be caused by incompatible drive/medium used.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl> <span data-ttu-id="c9b4e-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt> (HRESULT) 0xC0AA020F</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AA020F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-184">媒體的速度與裝置不相容。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-184">The media's speed is incompatible with the device.</span></span> <span data-ttu-id="c9b4e-185">這可能是因為使用較高或較低的速度媒體，而不是裝置支援的速度範圍。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-185">This may be caused by using higher or lower speed media than the range of speeds supported by the device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl> <span data-ttu-id="c9b4e-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt> (HRESULT) 0xC0AA0210</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT)0xC0AA0210</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-187">上次操作期間與此錄製器相關聯的裝置已被獨佔鎖定，導致此作業失敗。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-187">The device associated with this recorder during the last operation has been exclusively locked, causing this operation to fail.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl> <span data-ttu-id="c9b4e-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA0211</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0211</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-189">用戶端名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-189">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl> <span data-ttu-id="c9b4e-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt> (HRESULT) 0xC0AA02FF</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA02FF</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-191">裝置針對命令回報了未預期或不正確資料。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-191">The device reported unexpected or invalid data for a command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl> <span data-ttu-id="c9b4e-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt> (HRESULT) 0xC0AA0300</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT)0xC0AA0300</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-193">寫入失敗，因為磁片磁碟機無法快速地接收資料來繼續寫入。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-193">The write failed because the drive did not receive data quickly enough to continue writing.</span></span> <span data-ttu-id="c9b4e-194">將來源資料移至本機電腦、減少寫入速度，或啟用 &quot; 緩衝區不足的可用設定， &quot; 即可解決此問題。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-194">Moving the source data to the local computer, reducing the write speed, or enabling a &quot;buffer underrun free&quot; setting may resolve this issue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl> <span data-ttu-id="c9b4e-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt> (HRESULT) 0xC0AA0301</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA0301</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-196">寫入失敗，因為磁片磁碟機傳回無法從中復原的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-196">The write failed because the drive returned error information that could not be recovered from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl> <span data-ttu-id="c9b4e-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0400</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0400</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-198">目前正在進行寫入作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-198">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl> <span data-ttu-id="c9b4e-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0401</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0401</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-200">目前沒有任何寫入作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-200">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl> <span data-ttu-id="c9b4e-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt> (HRESULT) 0xC0AA0402</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT)0xC0AA0402</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-202">要求的作業僅適用于支援的媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-202">The requested operation is only valid with supported media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl> <span data-ttu-id="c9b4e-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0403</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0403</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-204">不支援提供要寫入的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-204">The provided stream to write is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl> <span data-ttu-id="c9b4e-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt> (HRESULT) 0xC0AA0404</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0404</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-206">提供要寫入的資料流程對目前插入的媒體而言太大。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-206">The provided stream to write is too large for the currently inserted media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl> <span data-ttu-id="c9b4e-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt> (HRESULT) 0xC0AA0405</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0405</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-208">若未將 ForceOverwrite 屬性設定為 VARIANT_TRUE，則不允許覆寫非空白媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-208">Overwriting non-blank media is not allowed without the ForceOverwrite property set to VARIANT_TRUE.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl> <span data-ttu-id="c9b4e-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0406</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0406</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-210">不支援目前的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-210">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl> <span data-ttu-id="c9b4e-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0407</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0407</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-212">此裝置不支援此光碟格式所需的作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-212">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl> <span data-ttu-id="c9b4e-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA0408</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0408</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-214">用戶端名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-214">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl> <span data-ttu-id="c9b4e-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0500</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0500</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-216">目前正在進行寫入作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-216">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl> <span data-ttu-id="c9b4e-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0501</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0501</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-218">目前沒有任何寫入作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-218">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl> <span data-ttu-id="c9b4e-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0502</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0502</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-220">只有在備妥媒體時，要求的作業才有效 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-220">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl> <span data-ttu-id="c9b4e-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0503</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0503</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-222">當媒體已備妥但未釋出時，要求的操作無效 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-222">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl> <span data-ttu-id="c9b4e-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt> (HRESULT) 0xC0AA0504</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT)0xC0AA0504</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-224">寫入媒體之後，就無法變更此屬性。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-224">The property cannot be changed once the media has been written to.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl> <span data-ttu-id="c9b4e-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt> (HRESULT) 0xC0AA0505</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AA0505</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-226">無法從空的光碟取出目錄。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-226">The table of contents cannot be retrieved from an empty disc.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl> <span data-ttu-id="c9b4e-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt> (HRESULT) 0xC0AA0506</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0506</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-228">僅支援空白的 CD-R/RW 媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-228">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl> <span data-ttu-id="c9b4e-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0507</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0507</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-230">僅支援空白的 CD-R/RW 媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-230">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl> <span data-ttu-id="c9b4e-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt> (HRESULT) 0xC0AA0508</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT)0xC0AA0508</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-232">CD-R 和 CD-RW 媒體最多支援99個音訊播放軌。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-232">CD-R and CD-RW media support a maximum of 99 audio tracks.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl> <span data-ttu-id="c9b4e-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt> (HRESULT) 0xC0AA0509</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0509</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-234">媒體上沒有足夠的空間可新增提供的音訊播放軌。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-234">There is not enough space left on the media to add the provided audio track.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl> <span data-ttu-id="c9b4e-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt> (HRESULT) 0xC0AA050A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA050A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-236">在選擇要使用的錄製器之前，您無法準備媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-236">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl> <span data-ttu-id="c9b4e-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt> (HRESULT) 0xC0AA050B</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT)0xC0AA050B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-238">提供的 ISRC 無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-238">The ISRC provided is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl> <span data-ttu-id="c9b4e-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt> (HRESULT) 0xC0AA050C</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT)0xC0AA050C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-240">提供的媒體目錄號碼無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-240">The Media Catalog Number provided is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl> <span data-ttu-id="c9b4e-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA050D</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-242">提供的音訊資料流程無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-242">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl> <span data-ttu-id="c9b4e-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA050E</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-244">此裝置不支援此光碟格式所需的作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-244">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl> <span data-ttu-id="c9b4e-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA050F</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA050F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-246">用戶端名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-246">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl> <span data-ttu-id="c9b4e-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0600</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0600</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-248">目前正在進行寫入作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-248">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl> <span data-ttu-id="c9b4e-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0601</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0601</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-250">目前沒有任何寫入作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-250">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl> <span data-ttu-id="c9b4e-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0602</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0602</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-252">只有在備妥媒體時，要求的作業才有效 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-252">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl> <span data-ttu-id="c9b4e-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0603</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0603</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-254">當媒體已備妥但未釋出時，要求的操作無效 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-254">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl> <span data-ttu-id="c9b4e-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA0604</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0604</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-256">用戶端名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-256">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl> <span data-ttu-id="c9b4e-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt> (HRESULT) 0xC0AA0606</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0606</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-258">僅支援空白的 CD-R/RW 媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-258">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl> <span data-ttu-id="c9b4e-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0607</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0607</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-260">僅支援空白的 CD-R/RW 媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-260">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl> <span data-ttu-id="c9b4e-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt> (HRESULT) 0xC0AA0609</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0609</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-262">媒體上的空間不足，無法新增提供的會話。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-262">There is not enough space on the media to add the provided session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl> <span data-ttu-id="c9b4e-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt> (HRESULT) 0xC0AA060A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA060A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-264">在選擇要使用的錄製器之前，您無法準備媒體。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-264">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl> <span data-ttu-id="c9b4e-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA060D</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-266">提供的音訊資料流程無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-266">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl> <span data-ttu-id="c9b4e-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA060E</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-268">目前的裝置不支援要求的資料區塊類型。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-268">The requested data block type is not supported by the current device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl> <span data-ttu-id="c9b4e-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt> (HRESULT) 0xC0AA060F</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT)0xC0AA060F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-270">串流在目前媒體的 leadin 中未包含足夠的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-270">The stream does not contain a sufficient number of sectors in the leadin for the current media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl> <span data-ttu-id="c9b4e-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0610</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0610</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-272">此裝置不支援此光碟格式所需的作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-272">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl> <span data-ttu-id="c9b4e-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt> (HRESULT) 0x80AA0900</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT)0x80AA0900</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-274">此格式目前正在使用光碟錄製器進行清除操作。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-274">The format is currently using the disc recorder for an erase operation.</span></span> <span data-ttu-id="c9b4e-275">請等候清除完成，再嘗試設定或清除目前的光碟錄製器。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-275">Please wait for the erase to complete before attempting to set or clear the current disc recorder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl> <span data-ttu-id="c9b4e-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt> (HRESULT) 0x80AA0901</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0901</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-277">清除格式只支援一個錄製器。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-277">The erase format only supports one recorder.</span></span> <span data-ttu-id="c9b4e-278">設定新的錄製器之前，您必須先清除目前的錄製器。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-278">You must clear the current recorder before setting a new one.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl> <span data-ttu-id="c9b4e-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt> (HRESULT) 0x80AA0902</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0902</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-280">磁片磁碟機未報告讀取光碟資訊命令的足夠資料。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-280">The drive did not report sufficient data for a READ DISC INFORMATION command.</span></span> <span data-ttu-id="c9b4e-281">可能不支援磁片磁碟機，或媒體可能不正確。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-281">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl> <span data-ttu-id="c9b4e-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt> (HRESULT) 0x80AA0903</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0903</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-283">磁片磁碟機未回報足夠的資料給模式感知 (頁面 0x2A) 命令。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-283">The drive did not report sufficient data for a MODE SENSE (page 0x2A) command.</span></span> <span data-ttu-id="c9b4e-284">可能不支援磁片磁碟機，或媒體可能不正確。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-284">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl> <span data-ttu-id="c9b4e-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt> (HRESULT) 0x80AA0904</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT)0x80AA0904</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-286">磁片磁碟機報告媒體無法擦擦。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-286">The drive reported that the media is not erasable.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl> <span data-ttu-id="c9b4e-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt> (HRESULT) 0x80AA0905</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0905</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-288">磁片磁碟機無法清除命令。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-288">The drive failed the erase command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl> <span data-ttu-id="c9b4e-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt> (HRESULT) 0x80AA0906</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT)0x80AA0906</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-290">磁片磁碟機未在一小時內完成清除。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-290">The drive did not complete the erase in one hour.</span></span> <span data-ttu-id="c9b4e-291">磁片磁碟機可能需要電源週期、媒體移除或其他手動介入，才能繼續適當的操作。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-291">The drive may require a power cycle, media removal, or other manual intervention to resume proper operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c9b4e-292">目前，如果嘗試透過 <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> 介面在 CD-RW 或 cd-rw 媒體上執行清除失敗，因為媒體不正確，也會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-292">Currently, this value will also be returned if an attempt to perform an erase on CD-RW or DVD-RW media via the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> interface fails as a result of the media being bad.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl> <span data-ttu-id="c9b4e-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt> (HRESULT) 0x80AA0907</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT)0x80AA0907</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-294">磁片磁碟機在清除期間傳回未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-294">The drive returned an unexpected error during the erase.</span></span> <span data-ttu-id="c9b4e-295">媒體可能無法使用、清除可能已完成，或磁片磁碟機可能仍在清除光碟的過程中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-295">The media may be unusable, the erase may be complete, or the drive may still be in the process of erasing the disc.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl> <span data-ttu-id="c9b4e-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt> (HRESULT) 0x80AA0908</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0908</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-297">磁片磁碟機傳回啟動單元 (spinup) 命令的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-297">The drive returned an error for a START UNIT (spinup) command.</span></span> <span data-ttu-id="c9b4e-298">可能需要手動介入。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-298">Manual intervention may be required.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl> <span data-ttu-id="c9b4e-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0909</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0909</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-300">不支援目前的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-300">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl> <span data-ttu-id="c9b4e-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA090A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA090A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-302">此裝置不支援此光碟格式所需的作業。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-302">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl> <span data-ttu-id="c9b4e-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA090B</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA090B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-304">用戶端名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-304">The client name is not valid.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c9b4e-305">下列成功和錯誤碼定義于 Imapi2fserror 中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-305">The following success and error codes are defined in Imapi2fserror.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c9b4e-306">常數/值</span><span class="sxs-lookup"><span data-stu-id="c9b4e-306">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c9b4e-307">Description</span><span class="sxs-lookup"><span data-stu-id="c9b4e-307">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl> <span data-ttu-id="c9b4e-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt> (HRESULT) 0xC0AAB100</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-309">發生內部錯誤： %1！ ls！。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-309">Internal error occurred: %1!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl> <span data-ttu-id="c9b4e-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt> (HRESULT) 0xC0AAB101</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT)0xC0AAB101</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-311">為參數 ' %1！ ls！ ' 指定的值</span><span class="sxs-lookup"><span data-stu-id="c9b4e-311">The value specified for parameter '%1!ls!'</span></span> <span data-ttu-id="c9b4e-312">無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-312">is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl> <span data-ttu-id="c9b4e-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt> (HRESULT) 0xC0AAB102</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT)0xC0AAB102</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-314">FileSystemImage 物件處於唯讀模式。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-314">FileSystemImage object is in read only mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl> <span data-ttu-id="c9b4e-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt> (HRESULT) 0xC0AAB103</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT)0xC0AAB103</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-316">未指定輸出檔案系統。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-316">No output file system specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl> <span data-ttu-id="c9b4e-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt> (HRESULT) 0xC0AAB104</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT)0xC0AAB104</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-318">指定的磁片區識別碼太長，或包含一或多個不正確字元。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-318">The specified Volume Identifier is either too long or contains one or more invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl> <span data-ttu-id="c9b4e-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt> (HRESULT) 0xC0AAB105</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT)0xC0AAB105</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-320">不正確檔案日期。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-320">Invalid file dates.</span></span> <span data-ttu-id="c9b4e-321">%1！ ls！</span><span class="sxs-lookup"><span data-stu-id="c9b4e-321">%1!ls!</span></span> <span data-ttu-id="c9b4e-322">時間早于 %2！ ls！</span><span class="sxs-lookup"><span data-stu-id="c9b4e-322">time is earlier than %2!ls!</span></span> <span data-ttu-id="c9b4e-323">時間的多個數列。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-323">time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl> <span data-ttu-id="c9b4e-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt> (HRESULT) 0xC0AAB106</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB106</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-325">此函數的檔案系統必須為空白。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-325">The file system must be empty for this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl> <span data-ttu-id="c9b4e-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt> (HRESULT) 0xC0AAB163L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB163L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-327">您無法變更為建立所指定的檔案系統，因為匯入會話中的檔案系統與目前會話中的檔案系統不符。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-327">You cannot change the file system specified for creation, because the file system from the imported session and the file system in the current session do not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl> <span data-ttu-id="c9b4e-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt> (HRESULT) 0xC0AAB108</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT)0xC0AAB108</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-329">指定的路徑 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-329">Specified path '%1!ls!'</span></span> <span data-ttu-id="c9b4e-330">未識別檔案。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-330">does not identify a file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl> <span data-ttu-id="c9b4e-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt> (HRESULT) 0xC0AAB109</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT)0xC0AAB109</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-332">指定的路徑 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-332">Specified path '%1!ls!'</span></span> <span data-ttu-id="c9b4e-333">未識別目錄。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-333">does not identify a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl> <span data-ttu-id="c9b4e-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt> (HRESULT) 0xC0AAB10A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB10A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-335">目錄 ' %1！ s！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-335">The directory '%1!s!'</span></span> <span data-ttu-id="c9b4e-336">不是空的。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-336">is not empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl> <span data-ttu-id="c9b4e-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt> (HRESULT) 0xC0AAB10B</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB10B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-338">ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-338">ls!'</span></span> <span data-ttu-id="c9b4e-339">不是檔案系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-339">is not part of the file system.</span></span> <span data-ttu-id="c9b4e-340">必須新增才能完成此操作。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-340">It must be added to complete this operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl> <span data-ttu-id="c9b4e-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt> (HRESULT) 0xC0AAB110</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT)0xC0AAB110</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-342">路徑 ' %1！ s！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-342">Path '%1!s!'</span></span> <span data-ttu-id="c9b4e-343">的格式不正確，或包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-343">is badly formed or contains invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl> <span data-ttu-id="c9b4e-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt> (HRESULT) 0xC0AAB111</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT)0xC0AAB111</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-345">名稱 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-345">The name '%1!ls!'</span></span> <span data-ttu-id="c9b4e-346">指定的不是合法：設定 UseRestrictedCharacterSet 屬性時所建立的檔案或目錄物件的名稱，可能只包含 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-346">specified is not legal: Name of file or directory object created while the UseRestrictedCharacterSet property is set may only contain ANSI characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl> <span data-ttu-id="c9b4e-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt> (HRESULT) 0xC0AAB112</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT)0xC0AAB112</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-348">ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-348">ls!'</span></span> <span data-ttu-id="c9b4e-349">名稱已存在。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-349">name already exists.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl> <span data-ttu-id="c9b4e-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt> (HRESULT) 0xC0AAB113</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT)0xC0AAB113</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-351">嘗試加入 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-351">Attempt to add '%1!ls!'</span></span> <span data-ttu-id="c9b4e-352">failed：無法為 %2！ ls！建立檔案系統特有的唯一名稱</span><span class="sxs-lookup"><span data-stu-id="c9b4e-352">failed: cannot create a file-system-specific unique name for the %2!ls!</span></span> <span data-ttu-id="c9b4e-353">檔案系統)。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-353">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl> <span data-ttu-id="c9b4e-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB118</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB118</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-355">找不到專案 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-355">Cannot find item '%1!ls!'</span></span> <span data-ttu-id="c9b4e-356">在 FileSystemImage 階層中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-356">in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl> <span data-ttu-id="c9b4e-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB119</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB119</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-358">檔案 ' %1！ s！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-358">The file '%1!s!'</span></span> <span data-ttu-id="c9b4e-359">在 FileSystemImage 階層中找不到。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-359">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl> <span data-ttu-id="c9b4e-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB11A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB11A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-361">目錄 ' %1！ s！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-361">The directory '%1!s!'</span></span> <span data-ttu-id="c9b4e-362">在 FileSystemImage 階層中找不到。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-362">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl> <span data-ttu-id="c9b4e-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt> (HRESULT) 0xC0AAB120</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT)0xC0AAB120</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-364">正在加入 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-364">Adding '%1!ls!'</span></span> <span data-ttu-id="c9b4e-365">結果影像的大小會大於目前設定的限制。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-365">would result in a result image having a size larger than the current configured limit.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl> <span data-ttu-id="c9b4e-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt> (HRESULT) 0xC0AAB121</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB121</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-367">針對 FreeMediaBlocks 屬性指定的值對於以目前資料為基礎的估計影像大小而言太小。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-367">Value specified for FreeMediaBlocks property is too small for estimated image size based on current data.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl> <span data-ttu-id="c9b4e-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt> (HRESULT) 0xC0AAB200L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT)0xC0AAB200L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-369">影像未在2kb 磁區界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-369">The image is not aligned on a 2kb sector boundary.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl> <span data-ttu-id="c9b4e-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB201L) </dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB201L)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-371">映射未包含有效的磁片區描述項。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-371">The image does not contain a valid volume descriptor.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl> <span data-ttu-id="c9b4e-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt> (HRESULT) 0xC0AAB202L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT)0xC0AAB202L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-373">在呼叫<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager：： Validate</strong></a>方法之前，尚未使用<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager：： SetPath</strong></a>或<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager：： SetStream</strong></a>方法設定影像。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-373">The image has not been set using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> methods prior to calling the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl> <span data-ttu-id="c9b4e-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt> (HRESULT) 0xC0AAB203L</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB203L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-375">提供的映射太大，無法進行驗證，因為大小超過 <strong>MAXLONG</strong>。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-375">The provided image is too large to be validated as the size exceeds <strong>MAXLONG</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl> <span data-ttu-id="c9b4e-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt> (HRESULT) 0xC0AAB128</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT)0xC0AAB128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-377">為檔案 ' %1！ ls！ ' 提供的資料流程</span><span class="sxs-lookup"><span data-stu-id="c9b4e-377">Data stream supplied for file '%1!ls!'</span></span> <span data-ttu-id="c9b4e-378">不一致：應為 %2！I64d!</span><span class="sxs-lookup"><span data-stu-id="c9b4e-378">is inconsistent: expected %2!I64d!</span></span> <span data-ttu-id="c9b4e-379">位元組，找到 %3！I64d！。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-379">bytes, found %3!I64d!.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl> <span data-ttu-id="c9b4e-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB129</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB129</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-381">無法從為檔案 ' %1！ ls！ ' 提供的資料流程讀取資料。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-381">Cannot read data from stream supplied for file '%1!ls!'.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl> <span data-ttu-id="c9b4e-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB12A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-383">嘗試建立檔案 ' %1！ ls！ ' 的資料流程時，發生下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="c9b4e-383">The following error was encountered when trying to create data stream for file '%1!ls!':</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl> <span data-ttu-id="c9b4e-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB12BL</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12BL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-385">因為許可權的緣故，無法在目錄樹狀結構中列舉檔案。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-385">Failure enumerating files in the directory tree is inaccessible due to permissions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl> <span data-ttu-id="c9b4e-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt> (HRESULT) 0xC0AAB130</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT)0xC0AAB130</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-387">%1！ ls！的這個檔案系統映射有太多目錄</span><span class="sxs-lookup"><span data-stu-id="c9b4e-387">This file system image has too many directories for the %1!ls!</span></span> <span data-ttu-id="c9b4e-388">檔案系統)。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-388">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl> <span data-ttu-id="c9b4e-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt> (HRESULT) 0xC0AAB131</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT)0xC0AAB131</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-390">ISO9660 限制為8個目錄層級。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-390">ISO9660 is limited to 8 levels of directories.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl> <span data-ttu-id="c9b4e-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt> (HRESULT) 0xC0AAB132</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB132</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-392">資料檔案對 ' %1！ ls！ ' 而言太大</span><span class="sxs-lookup"><span data-stu-id="c9b4e-392">Data file is too large for '%1!ls!'</span></span> <span data-ttu-id="c9b4e-393">檔案系統)。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-393">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl> <span data-ttu-id="c9b4e-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB138</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB138</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-395">無法初始化 %1！ ls！</span><span class="sxs-lookup"><span data-stu-id="c9b4e-395">Cannot initialize %1!ls!</span></span> <span data-ttu-id="c9b4e-396">隱藏盤案。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-396">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl> <span data-ttu-id="c9b4e-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB139</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB139</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-398">在 ' %1！ ls！ ' 中搜尋時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="c9b4e-398">Error seeking in '%1!ls!'</span></span> <span data-ttu-id="c9b4e-399">隱藏盤案。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-399">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl> <span data-ttu-id="c9b4e-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB13A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-401">寫入 ' %1！ ls！ ' 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="c9b4e-401">Error encountered writing to '%1!ls!'</span></span> <span data-ttu-id="c9b4e-402">隱藏盤案。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-402">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl> <span data-ttu-id="c9b4e-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB13B</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-404">從 ' %1！ ls！ ' 讀取時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="c9b4e-404">Error encountered reading from '%1!ls!'</span></span> <span data-ttu-id="c9b4e-405">隱藏盤案。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-405">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl> <span data-ttu-id="c9b4e-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt> (HRESULT) 0xC0AAB140</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB140</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-407">工作目錄 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-407">The working directory '%1!ls!'</span></span> <span data-ttu-id="c9b4e-408">無效。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-408">is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl> <span data-ttu-id="c9b4e-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt> (HRESULT) 0xC0AAB141</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT)0xC0AAB141</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-410">無法將工作目錄設定為 ' %1！ ls！ '。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-410">Cannot set working directory to '%1!ls!'.</span></span> <span data-ttu-id="c9b4e-411">可用的空間為 %2！I64d!</span><span class="sxs-lookup"><span data-stu-id="c9b4e-411">Space available is %2!I64d!</span></span> <span data-ttu-id="c9b4e-412">位元組，大約 %3！I64d!</span><span class="sxs-lookup"><span data-stu-id="c9b4e-412">bytes, approximately %3!I64d!</span></span> <span data-ttu-id="c9b4e-413">需要的位元組。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-413">bytes required.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl> <span data-ttu-id="c9b4e-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt> (HRESULT) 0xC0AAB142</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT)0xC0AAB142</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-415">嘗試將資料隱藏檔案移至目錄 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-415">Attempt to move the data stash file to directory '%1!ls!'</span></span> <span data-ttu-id="c9b4e-416">失敗。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-416">was not successful.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl> <span data-ttu-id="c9b4e-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt> (HRESULT) 0xC0AAB148</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT)0xC0AAB148</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-418">無法將開機物件新增至映射。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-418">The boot object could not be added to the image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl> <span data-ttu-id="c9b4e-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt> (HRESULT) 0xC0AAB149</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT)0xC0AAB149</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-420">開機物件只能包含在初始光碟映射中。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-420">A boot object can only be included in an initial disc image.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl> <span data-ttu-id="c9b4e-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt> (HRESULT) 0xC0AAB14A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB14A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-422">要求的模擬類型與開機映射大小不符。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-422">The emulation type requested does not match the boot image size.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl> <span data-ttu-id="c9b4e-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt> (HRESULT) 0xC0AAB150</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AAB150</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-424">光學媒體是空的。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-424">Optical media is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl> <span data-ttu-id="c9b4e-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt> (HRESULT) 0xC0AAB151</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB151</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-426">指定的光碟未包含其中一個支援的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-426">The specified disc does not contain one of the supported file systems.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl> <span data-ttu-id="c9b4e-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB152</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB152</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-428">指定的光碟未包含 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-428">The specified disc does not contain a '%1!ls!'</span></span> <span data-ttu-id="c9b4e-429">檔案系統)。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-429">file system.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl> <span data-ttu-id="c9b4e-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt> (HRESULT) 0xC0AAB153</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB153</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-431">匯入 ' %1！ ls！ ' 時發生一致性錯誤</span><span class="sxs-lookup"><span data-stu-id="c9b4e-431">Consistency error encountered while importing the '%1!ls!'</span></span> <span data-ttu-id="c9b4e-432">檔案系統)。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-432">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl> <span data-ttu-id="c9b4e-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AAB154</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AAB154</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-434">' %1！ ls！ '所選光碟上的檔案系統包含匯入： %2！ ls！不支援的功能。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-434">The '%1!ls!'file system on the selected disc contains a feature not supported for import: %2!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl> <span data-ttu-id="c9b4e-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt> (HRESULT) 0xC0AAB155</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB155</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-436">無法匯入 %2！ ls！</span><span class="sxs-lookup"><span data-stu-id="c9b4e-436">Could not import %2!ls!</span></span> <span data-ttu-id="c9b4e-437">磁片的檔案系統。檔案 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-437">file system from disc. The file '%1!ls!'</span></span> <span data-ttu-id="c9b4e-438">已存在於映射階層中做為目錄。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-438">already exists within the image hierarchy as a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl> <span data-ttu-id="c9b4e-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB156</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB156</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-440">無法搜尋以封鎖 %1！I64d!</span><span class="sxs-lookup"><span data-stu-id="c9b4e-440">Cannot seek to block %1!I64d!</span></span> <span data-ttu-id="c9b4e-441">在來源光碟上。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-441">on source disc.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl> <span data-ttu-id="c9b4e-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB157</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB157</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-443">從上一個會話匯入失敗，因為讀取媒體上的區塊時發生錯誤 (很可能會封鎖 %1！ u！ ) 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-443">Import from previous session failed due to an error reading a block on the media (most likely block %1!u!).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl> <span data-ttu-id="c9b4e-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt> (HRESULT) 0xC0AAB158</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB158</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-445">目前的光碟與匯入檔案系統的磁片不同。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-445">Current disc is not the same one from which file system was imported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl> <span data-ttu-id="c9b4e-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt> (HRESULT) 0xC0AAB159</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB159</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-447">IMAPI.EXE 不允許具有目前媒體類型的多重會話。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-447">IMAPI does not allow multi-session with the current media type.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl> <span data-ttu-id="c9b4e-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt> (HRESULT) 0xC0AAB15A</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AAB15A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-449">IMAPI.EXE 無法執行與目前媒體的多重會話，因為它不支援寫入的相容 UDF 修訂。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-449">IMAPI cannot do multi-session with the current media because it does not support a compatible UDF revision for write.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl> <span data-ttu-id="c9b4e-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt> (HRESULT) 0xC0AAB15B</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-451">IMAPI.EXE 不支援所要求的多會話型別。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-451">IMAPI does not support the multisession type requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl> <span data-ttu-id="c9b4e-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt> (HRESULT) 0xC0AAB133</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT)0xC0AAB133</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-453">作業失敗，因為先前從媒體匯入會話的版面配置不相容。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-453">Operation failed due to an incompatible layout of the previous session imported from the medium.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl> <span data-ttu-id="c9b4e-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt> (HRESULT) 0xC0AAB15C</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-455">IMAPI.EXE 不支援目前媒體上提供的任何多會話類型 (s) 。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-455">IMAPI supports none of the multisession type(s) provided on the current media.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c9b4e-456">[<strong>IFileSystemImage：： ImportFileSystem</strong>] (如果錄製裝置中沒有媒體，則/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) 方法會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-456">[<strong>IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method returns this error if there is no media in the recording device.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl> <span data-ttu-id="c9b4e-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt> (HRESULT) 0xC0AAB15D</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT)0xC0AAB15D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-458">MultisessionInterfaces 屬性必須在呼叫這個方法之前設定。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-458">MultisessionInterfaces property must be set prior calling this method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl> <span data-ttu-id="c9b4e-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt> (HRESULT) 0xC0AAB15E</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT)0xC0AAB15E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-460">無法匯入 %2！ ls！</span><span class="sxs-lookup"><span data-stu-id="c9b4e-460">Could not import %2!ls!</span></span> <span data-ttu-id="c9b4e-461">磁片的檔案系統。目錄 ' %1！ ls！ '</span><span class="sxs-lookup"><span data-stu-id="c9b4e-461">file system from disc. The directory '%1!ls!'</span></span> <span data-ttu-id="c9b4e-462">已在映射階層內以檔案形式存在。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-462">already exists within the image hierarchy as a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl> <span data-ttu-id="c9b4e-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt> (HRESULT) 0xC0AAB162</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT)0xC0AAB162</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-464">無法抓取其中一個多會話參數或其值錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-464">One of multisession parameters cannot be retrieved or has a wrong value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl> <span data-ttu-id="c9b4e-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0x00AAB15FL</dt> </span><span class="sxs-lookup"><span data-stu-id="c9b4e-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x00AAB15FL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9b4e-466">目前的檔案系統版本不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-466">This feature is not supported for the current file system revision.</span></span> <span data-ttu-id="c9b4e-467">建立映射時不會有這項功能。</span><span class="sxs-lookup"><span data-stu-id="c9b4e-467">The image will be created without this feature.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c9b4e-468">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9b4e-468">Requirements</span></span>



| <span data-ttu-id="c9b4e-469">需求</span><span class="sxs-lookup"><span data-stu-id="c9b4e-469">Requirement</span></span> | <span data-ttu-id="c9b4e-470">值</span><span class="sxs-lookup"><span data-stu-id="c9b4e-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b4e-471">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9b4e-471">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b4e-472">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9b4e-472">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c9b4e-473">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9b4e-473">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b4e-474">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9b4e-474">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                            |
| <span data-ttu-id="c9b4e-475">標頭</span><span class="sxs-lookup"><span data-stu-id="c9b4e-475">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b4e-476"><dt>Imapi2error .h;</dt><dt>Imapi2fserror .h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b4e-476"><dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt></span></span> </dl> |



 

 





