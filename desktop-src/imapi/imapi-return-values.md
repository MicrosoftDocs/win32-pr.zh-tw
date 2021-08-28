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
ms.openlocfilehash: 857f9c018fc34a16a0dc431714aacc1fcdf6a5b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474794"
---
# <a name="imapi-return-values"></a>IMAPI.EXE 傳回值

IMAPI.EXE 方法會傳回非負數值， (通常會 \_ 在方法成功時) 正常。 當失敗時，IMAPI.EXE 方法會傳回 Winerror.h .h、Imapi2error 或 Imapi2fserror 的成功或錯誤碼。

已定義下列成功和錯誤碼。




| 常數/值 | Description | 
|----------------|-------------|
| <span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt> (HRESULT) 0xC0AA0007L</dt></dl> | 光碟未通過燒錄驗證，可能包含損毀的資料或無法使用。<br /> | 
| <span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt> (HRESULT) 0xC0AA0002</dt></dl> | 已取消要求。<br /> | 
| <span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt> (HRESULT) 0xC0AA0003</dt></dl> | 要求必須選取目前的光碟錄製器。<br /> | 
| <span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0x00AA0302L</dt></dl> | 目前沒有任何寫入作業正在進行中。<br /> | 
| <span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt> (HRESULT) 0x00AA0004</dt></dl> | 磁片磁碟機不支援要求的寫入速度，並且已調整速度。<br /> | 
| <span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt> (HRESULT) 0x00AA0005</dt></dl> | 磁片磁碟機不支援要求的旋轉類型，且已調整旋轉類型。<br /> | 
| <span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt> (HRESULT) 0x00AA0006</dt></dl> | 磁片磁碟機不支援要求的寫入速度和旋轉類型，而且兩者都經過調整。<br /> | 
| <span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt> (HRESULT) 0x00AA0200</dt></dl> | 裝置已接受命令，但傳回的意義資料表示錯誤。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt> (HRESULT) 0x80AA0A00L</dt></dl> | 因為呼叫 <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator：： CreateResultImage</strong></a>，所以映射已變成隻讀。 因此無法再修改物件。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt> (HRESULT) 0x80AA0A01L</dt></dl> | 可能不會再新增任何曲目。 CD 媒體的範圍限制為1-99 個曲目。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt> (HRESULT) 0x80AA0A03L</dt></dl> | 使用此函式之前，必須先將追蹤新增至影像。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0x80AA0A02L</dt></dl> | 不支援要求的磁區類型。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt> (HRESULT) 0x80AA0A04L</dt></dl> | 使用此函式之前，可能不會將追蹤新增至影像。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt> (HRESULT) 0x80AA0A05L</dt></dl> | 新增此播放軌會超過 leadout 開頭的限制。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt> (HRESULT) 0x80AA0A06L</dt></dl> | 新增此播放軌會超過99索引限制。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt> (HRESULT) 0x80AA0A07L</dt></dl> | 指定的 LBA 位移不在追蹤索引的清單中。<br /> | 
| <span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt> (HRESULT) 0x00AA0A08L</dt></dl> | 指定的 LBA 位移已經在追蹤索引的清單中。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt> (HRESULT) 0x80AA0A09L</dt></dl> | 無法清除索引 1 (LBA offset 0) 。<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt> (HRESULT) 0x80AA0A0AL</dt></dl> | 每個索引都必須有10個磁區的最小大小。<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt> (HRESULT) 0xC0AA0201</dt></dl> | 裝置回報要求的模式頁面 (，且類型) 不存在。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt> (HRESULT) 0xC0AA0202</dt></dl> | 裝置中沒有任何媒體。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt> (HRESULT) 0xC0AA0203</dt></dl> | 媒體與未知的實體格式不相容。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt> (HRESULT) 0xC0AA0204</dt></dl> | 媒體會朝下插入。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt> (HRESULT) 0xC0AA0205</dt></dl> | 磁片磁碟機回報正在準備就緒。 請稍後再試一次要求。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0206</dt></dl> | 媒體目前正在格式化。 請等候格式完成，再嘗試使用媒體。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt> (HRESULT) 0xC0AA0207</dt></dl> | 磁片磁碟機回報它正在執行長時間執行的作業，例如完成寫入。 磁片磁碟機可能很長一段時間無法使用。<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt> (HRESULT) 0xC0AA0208</dt></dl> | 磁片磁碟機回報，不支援在模式選取命令的模式頁面中提供的參數組合。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt> (HRESULT) 0xC0AA0209</dt></dl> | 磁片磁碟機報告媒體已受寫入保護。<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt> (HRESULT) 0xC0AA020A</dt></dl> | 裝置不支援要求的功能頁面。<br /> | 
| <span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt> (HRESULT) 0xC0AA020B</dt></dl> | 支援要求的功能頁面，但未標示為最新。<br /> | 
| <span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA020C</dt></dl> | 磁片磁碟機不支援 GET CONFIGURATION 命令。<br /> | 
| <span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt> (HRESULT) 0xC0AA020D</dt></dl> | 裝置無法接受超時時間內的命令。 這可能是因為裝置進入不一致的狀態，或命令的超時值可能需要增加。<br /> | 
| <span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt> (HRESULT) 0xC0AA020E</dt></dl> | DVD 結構不存在。 這可能是因為使用的驅動程式/媒體不相容所造成。<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt> (HRESULT) 0xC0AA020F</dt></dl> | 媒體的速度與裝置不相容。 這可能是因為使用較高或較低的速度媒體，而不是裝置支援的速度範圍。<br /> | 
| <span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt> (HRESULT) 0xC0AA0210</dt></dl> | 上次操作期間與此錄製器相關聯的裝置已被獨佔鎖定，導致此作業失敗。<br /> | 
| <span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA0211</dt></dl> | 用戶端名稱無效。<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt> (HRESULT) 0xC0AA02FF</dt></dl> | 裝置針對命令回報了未預期或不正確資料。<br /> | 
| <span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt> (HRESULT) 0xC0AA0300</dt></dl> | 寫入失敗，因為磁片磁碟機無法快速地接收資料來繼續寫入。 將來源資料移至本機電腦、減少寫入速度，或啟用「無緩衝區不足」設定，可能會解決此問題。<br /> | 
| <span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt> (HRESULT) 0xC0AA0301</dt></dl> | 寫入失敗，因為磁片磁碟機傳回無法從中復原的錯誤資訊。<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0400</dt></dl> | 目前正在進行寫入作業。<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0401</dt></dl> | 目前沒有任何寫入作業正在進行中。<br /> | 
| <span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt> (HRESULT) 0xC0AA0402</dt></dl> | 要求的作業僅適用于支援的媒體。<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0403</dt></dl> | 不支援提供要寫入的資料流程。<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt> (HRESULT) 0xC0AA0404</dt></dl> | 提供要寫入的資料流程對目前插入的媒體而言太大。<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt> (HRESULT) 0xC0AA0405</dt></dl> | 若未將 ForceOverwrite 屬性設定為 VARIANT_TRUE，則不允許覆寫非空白媒體。<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0406</dt></dl> | 不支援目前的媒體類型。<br /> | 
| <span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0407</dt></dl> | 此裝置不支援此光碟格式所需的作業。<br /> | 
| <span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA0408</dt></dl> | 用戶端名稱無效。<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0500</dt></dl> | 目前正在進行寫入作業。<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0501</dt></dl> | 目前沒有任何寫入作業正在進行中。<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0502</dt></dl> | 只有當媒體已「備妥」時，要求的作業才有效。<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0503</dt></dl> | 當媒體「準備」但未釋出時，要求的作業無效。<br /> | 
| <span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt> (HRESULT) 0xC0AA0504</dt></dl> | 寫入媒體之後，就無法變更此屬性。<br /> | 
| <span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt> (HRESULT) 0xC0AA0505</dt></dl> | 無法從空的光碟取出目錄。<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt> (HRESULT) 0xC0AA0506</dt></dl> | 僅支援空白的 CD-R/RW 媒體。<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0507</dt></dl> | 僅支援空白的 CD-R/RW 媒體。<br /> | 
| <span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt> (HRESULT) 0xC0AA0508</dt></dl> | CD-R 和 CD-RW 媒體最多支援99個音訊播放軌。<br /> | 
| <span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt> (HRESULT) 0xC0AA0509</dt></dl> | 媒體上沒有足夠的空間可新增提供的音訊播放軌。<br /> | 
| <span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt> (HRESULT) 0xC0AA050A</dt></dl> | 在選擇要使用的錄製器之前，您無法準備媒體。<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt> (HRESULT) 0xC0AA050B</dt></dl> | 提供的 ISRC 無效。<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt> (HRESULT) 0xC0AA050C</dt></dl> | 提供的媒體目錄號碼無效。<br /> | 
| <span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA050D</dt></dl> | 提供的音訊資料流程無效。<br /> | 
| <span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA050E</dt></dl> | 此裝置不支援此光碟格式所需的作業。<br /> | 
| <span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA050F</dt></dl> | 用戶端名稱無效。<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0600</dt></dl> | 目前正在進行寫入作業。<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt> (HRESULT) 0xC0AA0601</dt></dl> | 目前沒有任何寫入作業正在進行中。<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0602</dt></dl> | 只有當媒體已「備妥」時，要求的作業才有效。<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt> (HRESULT) 0xC0AA0603</dt></dl> | 當媒體「準備」但未釋出時，要求的作業無效。<br /> | 
| <span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA0604</dt></dl> | 用戶端名稱無效。<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt> (HRESULT) 0xC0AA0606</dt></dl> | 僅支援空白的 CD-R/RW 媒體。<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0607</dt></dl> | 僅支援空白的 CD-R/RW 媒體。<br /> | 
| <span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt> (HRESULT) 0xC0AA0609</dt></dl> | 媒體上的空間不足，無法新增提供的會話。<br /> | 
| <span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt> (HRESULT) 0xC0AA060A</dt></dl> | 在選擇要使用的錄製器之前，您無法準備媒體。<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA060D</dt></dl> | 提供的音訊資料流程無效。<br /> | 
| <span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA060E</dt></dl> | 目前的裝置不支援要求的資料區塊類型。<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt> (HRESULT) 0xC0AA060F</dt></dl> | 串流在目前媒體的 leadin 中未包含足夠的磁區數目。<br /> | 
| <span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0610</dt></dl> | 此裝置不支援此光碟格式所需的作業。<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt> (HRESULT) 0x80AA0900</dt></dl> | 此格式目前正在使用光碟錄製器進行清除操作。 請等候清除完成，再嘗試設定或清除目前的光碟錄製器。<br /> | 
| <span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt> (HRESULT) 0x80AA0901</dt></dl> | 清除格式只支援一個錄製器。 設定新的錄製器之前，您必須先清除目前的錄製器。<br /> | 
| <span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt> (HRESULT) 0x80AA0902</dt></dl> | 磁片磁碟機未報告讀取光碟資訊命令的足夠資料。 可能不支援磁片磁碟機，或媒體可能不正確。<br /> | 
| <span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt> (HRESULT) 0x80AA0903</dt></dl> | 磁片磁碟機未回報足夠的資料給模式感知 (頁面 0x2A) 命令。 可能不支援磁片磁碟機，或媒體可能不正確。<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt> (HRESULT) 0x80AA0904</dt></dl> | 磁片磁碟機報告媒體無法擦擦。<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt> (HRESULT) 0x80AA0905</dt></dl> | 磁片磁碟機無法清除命令。<br /> | 
| <span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt> (HRESULT) 0x80AA0906</dt></dl> | 磁片磁碟機未在一小時內完成清除。 磁片磁碟機可能需要電源週期、媒體移除或其他手動介入，才能繼續適當的操作。<br /><blockquote>[!Note]<br />目前，如果嘗試透過 <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> 介面在 CD-RW 或 cd-rw 媒體上執行清除失敗，因為媒體不正確，也會傳回此值。</blockquote><br /> | 
| <span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt> (HRESULT) 0x80AA0907</dt></dl> | 磁片磁碟機在清除期間傳回未預期的錯誤。 媒體可能無法使用、清除可能已完成，或磁片磁碟機可能仍在清除光碟的過程中。<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt> (HRESULT) 0x80AA0908</dt></dl> | 磁片磁碟機傳回啟動單元 (spinup) 命令的錯誤。 可能需要手動介入。<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA0909</dt></dl> | 不支援目前的媒體類型。<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AA090A</dt></dl> | 此裝置不支援此光碟格式所需的作業。<br /> | 
| <span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt> (HRESULT) 0xC0AA090B</dt></dl> | 用戶端名稱無效。<br /> | 




下列成功和錯誤碼定義于 Imapi2fserror 中。




| 常數/值 | Description | 
|----------------|-------------|
| <span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt> (HRESULT) 0xC0AAB100</dt></dl> | 發生內部錯誤： %1！ ls！。<br /> | 
| <span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt> (HRESULT) 0xC0AAB101</dt></dl> | 為參數 ' %1！ ls！ ' 指定的值 無效。<br /> | 
| <span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl><dt><strong>IMAPI_E_READONLY</strong></dt> <dt> (HRESULT) 0xC0AAB102</dt></dl> | FileSystemImage 物件處於唯讀模式。<br /> | 
| <span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt> (HRESULT) 0xC0AAB103</dt></dl> | 未指定輸出檔案系統。<br /> | 
| <span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt> (HRESULT) 0xC0AAB104</dt></dl> | 指定的磁片區識別碼太長，或包含一或多個不正確字元。<br /> | 
| <span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt> (HRESULT) 0xC0AAB105</dt></dl> | 不正確檔案日期。 %1！ ls！ 時間早于 %2！ ls！ 時間的多個數列。<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt> (HRESULT) 0xC0AAB106</dt></dl> | 此函數的檔案系統必須為空白。<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt> (HRESULT) 0xC0AAB163L</dt></dl> | 您無法變更為建立所指定的檔案系統，因為匯入會話中的檔案系統與目前會話中的檔案系統不符。<br /> | 
| <span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt> (HRESULT) 0xC0AAB108</dt></dl> | 指定的路徑 ' %1！ ls！ ' 未識別檔案。<br /> | 
| <span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt> (HRESULT) 0xC0AAB109</dt></dl> | 指定的路徑 ' %1！ ls！ ' 未識別目錄。<br /> | 
| <span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt> (HRESULT) 0xC0AAB10A</dt></dl> | 目錄 ' %1！ s！ ' 不是空的。<br /> | 
| <span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt> (HRESULT) 0xC0AAB10B</dt></dl> | ls！ ' 不是檔案系統的一部分。 必須新增才能完成此操作。<br /> | 
| <span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt> (HRESULT) 0xC0AAB110</dt></dl> | 路徑 ' %1！ s！ ' 的格式不正確，或包含不正確字元。<br /> | 
| <span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt> (HRESULT) 0xC0AAB111</dt></dl> | 名稱 ' %1！ ls！ ' 指定的不是合法：設定 UseRestrictedCharacterSet 屬性時所建立的檔案或目錄物件的名稱，可能只包含 ANSI 字元。<br /> | 
| <span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt> (HRESULT) 0xC0AAB112</dt></dl> | ls！ ' 名稱已存在。<br /> | 
| <span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt> (HRESULT) 0xC0AAB113</dt></dl> | 嘗試加入 ' %1！ ls！ ' failed：無法為 %2！ ls！建立檔案系統特有的唯一名稱 檔案系統)。<br /> | 
| <span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB118</dt></dl> | 找不到專案 ' %1！ ls！ ' 在 FileSystemImage 階層中。<br /> | 
| <span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB119</dt></dl> | 檔案 ' %1！ s！ ' 在 FileSystemImage 階層中找不到。<br /> | 
| <span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB11A</dt></dl> | 目錄 ' %1！ s！ ' 在 FileSystemImage 階層中找不到。<br /> | 
| <span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt> (HRESULT) 0xC0AAB120</dt></dl> | 正在加入 ' %1！ ls！ ' 結果影像的大小會大於目前設定的限制。<br /> | 
| <span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt> (HRESULT) 0xC0AAB121</dt></dl> | 針對 FreeMediaBlocks 屬性指定的值對於以目前資料為基礎的估計影像大小而言太小。 <br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt> (HRESULT) 0xC0AAB200L</dt></dl> | 影像未在2kb 磁區界限上對齊。<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB201L) </dt></dl> | 映射未包含有效的磁片區描述項。<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt> (HRESULT) 0xC0AAB202L</dt></dl> | 在呼叫<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager：： Validate</strong></a>方法之前，尚未使用<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager：： SetPath</strong></a>或<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager：： SetStream</strong></a>方法設定影像。<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt> (HRESULT) 0xC0AAB203L</dt></dl> | 提供的映射太大，無法進行驗證，因為大小超過 <strong>MAXLONG</strong>。<br /> | 
| <span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt> (HRESULT) 0xC0AAB128</dt></dl> | 為檔案 ' %1！ ls！ ' 提供的資料流程 不一致：應為 %2！I64d! 位元組，找到 %3！I64d！。 <br /> | 
| <span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB129</dt></dl> | 無法從為檔案 ' %1！ ls！ ' 提供的資料流程讀取資料。<br /> | 
| <span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB12A</dt></dl> | 嘗試建立檔案 ' %1！ ls！ ' 的資料流程時，發生下列錯誤： <br /> | 
| <span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB12BL</dt></dl> | 因為許可權的緣故，無法在目錄樹狀結構中列舉檔案。<br /> | 
| <span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt> (HRESULT) 0xC0AAB130</dt></dl> | %1！ ls！的這個檔案系統映射有太多目錄 檔案系統)。<br /> | 
| <span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt> (HRESULT) 0xC0AAB131</dt></dl> | ISO9660 限制為8個目錄層級。<br /> | 
| <span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt> (HRESULT) 0xC0AAB132</dt></dl> | 資料檔案對 ' %1！ ls！ ' 而言太大 檔案系統)。<br /> | 
| <span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB138</dt></dl> | 無法初始化 %1！ ls！ 隱藏盤案。<br /> | 
| <span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB139</dt></dl> | 在 ' %1！ ls！ ' 中搜尋時發生錯誤 隱藏盤案。<br /> | 
| <span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB13A</dt></dl> | 寫入 ' %1！ ls！ ' 時發生錯誤 隱藏盤案。<br /> | 
| <span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB13B</dt></dl> | 從 ' %1！ ls！ ' 讀取時發生錯誤 隱藏盤案。<br /> | 
| <span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt> (HRESULT) 0xC0AAB140</dt></dl> | 工作目錄 ' %1！ ls！ ' 無效。<br /> | 
| <span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt> (HRESULT) 0xC0AAB141</dt></dl> | 無法將工作目錄設定為 ' %1！ ls！ '。 可用的空間為 %2！I64d! 位元組，大約 %3！I64d! 需要的位元組。 <br /> | 
| <span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt> (HRESULT) 0xC0AAB142</dt></dl> | 嘗試將資料隱藏檔案移至目錄 ' %1！ ls！ ' 失敗。<br /> | 
| <span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt> (HRESULT) 0xC0AAB148</dt></dl> | 無法將開機物件新增至映射。<br /> | 
| <span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt> (HRESULT) 0xC0AAB149</dt></dl> | 開機物件只能包含在初始光碟映射中。<br /> | 
| <span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt> (HRESULT) 0xC0AAB14A</dt></dl> | 要求的模擬類型與開機映射大小不符。<br /> | 
| <span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt> (HRESULT) 0xC0AAB150</dt></dl> | 光學媒體是空的。<br /> | 
| <span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt> (HRESULT) 0xC0AAB151</dt></dl> | 指定的光碟未包含其中一個支援的檔案系統。<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt> (HRESULT) 0xC0AAB152</dt></dl> | 指定的光碟未包含 ' %1！ ls！ ' 檔案系統)。<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt> (HRESULT) 0xC0AAB153</dt></dl> | 匯入 ' %1！ ls！ ' 時發生一致性錯誤 檔案系統)。<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0xC0AAB154</dt></dl> | ' %1！ ls！ '所選光碟上的檔案系統包含匯入： %2！ ls！不支援的功能。<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt> (HRESULT) 0xC0AAB155</dt></dl> | 無法匯入 %2！ ls！ 磁片的檔案系統。檔案 ' %1！ ls！ ' 已存在於映射階層中做為目錄。<br /> | 
| <span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB156</dt></dl> | 無法搜尋以封鎖 %1！I64d! 在來源光碟上。 <br /> | 
| <span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt> (HRESULT) 0xC0AAB157</dt></dl> | 從上一個會話匯入失敗，因為讀取媒體上的區塊時發生錯誤 (很可能會封鎖 %1！ u！ ) 。<br /> | 
| <span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt> (HRESULT) 0xC0AAB158</dt></dl> | 目前的光碟與匯入檔案系統的磁片不同。<br /> | 
| <span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt> (HRESULT) 0xC0AAB159</dt></dl> | IMAPI.EXE 不允許具有目前媒體類型的多重會話。<br /> | 
| <span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt> (HRESULT) 0xC0AAB15A</dt></dl> | IMAPI.EXE 無法執行與目前媒體的多重會話，因為它不支援寫入的相容 UDF 修訂。<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt> (HRESULT) 0xC0AAB15B</dt></dl> | IMAPI.EXE 不支援所要求的多會話型別。<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt> (HRESULT) 0xC0AAB133</dt></dl> | 作業失敗，因為先前從媒體匯入會話的版面配置不相容。<br /> | 
| <span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt> (HRESULT) 0xC0AAB15C</dt></dl> | IMAPI.EXE 不支援目前媒體上提供的任何多會話類型 (s) 。<br /><blockquote>[!Note]<br />如果錄製裝置中沒有媒體， [<strong>IFileSystemImage：： ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem)方法會傳回此錯誤。</blockquote><br /> | 
| <span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt> (HRESULT) 0xC0AAB15D</dt></dl> | MultisessionInterfaces 屬性必須在呼叫這個方法之前設定。<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt> (HRESULT) 0xC0AAB15E</dt></dl> | 無法匯入 %2！ ls！ 磁片的檔案系統。目錄 ' %1！ ls！ ' 已在映射階層內以檔案形式存在。<br /> | 
| <span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt> (HRESULT) 0xC0AAB162</dt></dl> | 無法抓取其中一個多會話參數或其值錯誤。<br /> | 
| <span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt> (HRESULT) 0x00AAB15FL</dt></dl> | 目前的檔案系統版本不支援這項功能。 建立映射時不會有這項功能。<br /> | 




## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                            |
| 標頭<br/>                   | <dl> <dt>Imapi2error .h;</dt><dt>Imapi2fserror .h</dt> </dl> |



 

 





