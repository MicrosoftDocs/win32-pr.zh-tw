---
description: 表示檔案記錄區段。 這是主要檔案資料表中的每個檔案記錄區段的標頭 (MFT) 。
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: FILE_RECORD_SEGMENT_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187610"
---
# <a name="file_record_segment_header-structure"></a>檔案 \_ 記錄 \_ 區段 \_ 標頭結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

表示檔案記錄區段。 這是主要檔案資料表中的每個檔案記錄區段的標頭 (MFT) 。

## <a name="syntax"></a>語法


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**MultiSectorHeader**
</dt> <dd>

快取管理員所定義的 multisector 標頭。 [**多 \_ 磁區 \_ 標頭**](multi-sector-header.md)結構一律會包含「檔案」簽章，以及更新順序陣列的位置和大小描述。

</dd> <dt>

**Reserved1**
</dt> <dd>

保留的。

</dd> <dt>

**SequenceNumber**
</dt> <dd>

序號。 每次釋放檔案記錄區段時，此值就會遞增;如果未使用區段，則為0。 檔案參考的 **SequenceNumber** 欄位必須符合此欄位的內容;如果不相符，則檔案參考不正確，而且可能已淘汰。

</dd> <dt>

**Reserved2**
</dt> <dd>

保留的。

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

第一個屬性記錄的位移，以位元組為單位。

</dd> <dt>

**旗標**
</dt> <dd>

檔案旗標。

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**檔案 \_\_ \_ \_ 使用中的記錄區段** (0x0001) 
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**檔案 \_檔案名 \_ \_ 索引 \_ 存在** (0x0002) 
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

保留的。

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

這個檔案的基底檔案記錄區段的檔案參考。 如果這是基底檔案記錄，則值為0。 請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。

</dd> <dt>

**Reserved4**
</dt> <dd>

保留的。

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

更新順序陣列，用來保護檔案記錄區段的 multisector 傳輸。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，此結構沒有相關聯的標頭檔。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
