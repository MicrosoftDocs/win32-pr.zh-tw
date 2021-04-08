---
title: 'BG_FILE_PROGRESS 結構 (>deliveryoptimization .h) '
description: BG_FILE_PROGRESS 結構會提供檔案相關的進度資訊，例如已傳送的位元組數目。
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS 結構
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686249"
---
# <a name="bg_file_progress-structure"></a>BG_FILE_PROGRESS 結構

**BG_FILE_PROGRESS** 結構會提供檔案相關的進度資訊，例如已傳送的位元組數目。

## <a name="syntax"></a>語法


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**BytesTotal**
</dt> <dd>

檔案大小，以位元組為單位。 如果無法判斷檔案的大小 (例如，如果檔案或伺服器) 不存在，則會 DO_UNKNOWN_FILE_SIZE 此值。

如果您是從檔案下載範圍， **BytesTotal** 會反映您想要從檔案下載的位元組總數。

</dd> <dt>

**BytesTransferred**
</dt> <dd>

傳送的位元組數目。

</dd> <dt>

**Completed**
</dt> <dd>

若為下載，當使用者可以使用檔案時，此值為 **TRUE** 。否則，此值為 **FALSE**。 在呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法之後，使用者可以使用檔案。 如果 **Complete** 方法產生暫時性錯誤，則在發生錯誤之前處理的那些檔案可供使用者使用;其他則否。 當 **完成** 失敗時，請使用 **完成** 的成員來判斷檔案是否可供使用者使用。

</dd> </dl>

## <a name="remarks"></a>備註

若要判斷是否已傳送檔案，您可以：

-   比較 **BytesTransferred** 與 **BytesTotal**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile：： GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





