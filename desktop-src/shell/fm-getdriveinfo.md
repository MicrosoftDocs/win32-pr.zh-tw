---
description: 由檔案管理員延伸模組所傳送，可從 [active File Manager] 視窗取出磁片磁碟機資訊。
title: 'FM_GETDRIVEINFO 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991075"
---
# <a name="fm_getdriveinfo-message"></a>FM \_ GETDRIVEINFO 訊息

由檔案管理員延伸模組所傳送，可從 [active File Manager] 視窗取出磁片磁碟機資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

接收磁片磁碟機資訊之 [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) 結構的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零。

## <a name="remarks"></a>備註

如果在 [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md)結構的 **dwTotalSpace** 或 **dwFreeSpace** 成員中傳回0xffffffff，則延伸模組程式庫必須計算值或值。

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

 

 




