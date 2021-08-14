---
description: 由檔管理程式延伸模組傳送，使檔管理程式重新繪製其使用中視窗或所有視窗。
title: 'FM_REFRESH_WINDOWS 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: fa38b55fdcd7c338102ed62bd9d7011ca4b7caf79fa81e834bcf915d8f934464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224264"
---
# <a name="fm_refresh_windows-message"></a>FM \_ REFRESH \_ WINDOWS 訊息

由檔管理程式延伸模組傳送，使檔管理程式重新繪製其使用中視窗或所有視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*fRepaint* 
</dt> <dd>

值，這個值會指出檔管理程式是否會重新繪製其使用中視窗或所有視窗。 如果此參數為 **TRUE**，則 [檔案管理員] 會重新繪製其所有視窗。 否則，[檔案管理員] 只會重繪其使用中視窗。

</dd> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

檔案管理員會自動偵測延伸模組所造成的檔案系統變更。 只有在建立或取消磁片磁碟機連線的情況下，延伸模組才應該使用此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




