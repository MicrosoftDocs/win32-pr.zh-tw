---
description: 代表主要檔案資料表中 (MFT) 的位址。 位址會以迴圈的重複使用序號標記，此序號是在 MFT 區段參考有效時所設定。
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: MFT_SEGMENT_REFERENCE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109929"
---
# <a name="mft_segment_reference-structure"></a>MFT \_ 區段 \_ 參考結構

\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]

代表主要檔案資料表中 (MFT) 的位址。 位址會以迴圈的重複使用序號標記，此序號是在 MFT 區段參考有效時所設定。

## <a name="syntax"></a>語法


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>成員

<dl> <dt>

**SegmentNumberLowPart**
</dt> <dd>

區段編號的低部分。

</dd> <dt>

**SegmentNumberHighPart**
</dt> <dd>

區段編號的最高部分。

</dd> <dt>

**SequenceNumber**
</dt> <dd>

非零的序號。 0值為 reserved。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，此結構沒有相關聯的標頭檔。

此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。

檔案 **\_ 參考** 資料類型的定義如下。

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[主檔案資料表](master-file-table.md)
</dt> </dl>

 

 
