---
title: 'BG_JOB_PROGRESS 結構 (>deliveryoptimization .h) '
description: BG_JOB_PROGRESS 結構會提供作業相關的進度資訊，例如已傳送的位元組和檔案數目。 針對上傳作業，進度會套用至上傳檔案，而不是回復檔。
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- BG_JOB_PROGRESS 結構
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509088"
---
# <a name="bg_job_progress-structure"></a>BG_JOB_PROGRESS 結構

**BG_JOB_PROGRESS** 結構會提供作業相關的進度資訊，例如已傳送的位元組和檔案數目。 針對上傳作業，進度會套用至上傳檔案，而不是回復檔。

## <a name="syntax"></a>語法


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**BytesTotal**
</dt> <dd>

要針對作業中的所有檔案傳送的總位元組數。 如果值為 BG_SIZE_UNKNOWN，則不會判斷作業中所有檔案的總大小。 如果無法判斷其中一個檔案的大小，則不會設定此值。 例如，如果指定的檔案或伺服器不存在，就無法判斷檔案的大小。

如果您要從檔案下載範圍， **BytesTotal** 會包含您想要從檔案下載的位元組總數。

</dd> <dt>

**BytesTransferred**
</dt> <dd>

傳送的位元組數目。

</dd> <dt>

**FilesTotal**
</dt> <dd>

要針對此作業傳送的檔案總數。

</dd> <dt>

**FilesTransferred**
</dt> <dd>

傳輸的檔案數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyJob：： GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





