---
description: 由檔案管理員延伸模組所傳送，可在 [active File Manager] 視窗中取出選取的檔案數目 (目錄視窗或 [搜尋結果] 視窗) 。 計數包括具有長檔名的檔案。
title: 'FM_GETSELCOUNTLFN 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: ff0884e1b80e4a5a7e6c295bd449c8e1f6d069ced6c988f584108318a98c6891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094173"
---
# <a name="fm_getselcountlfn-message"></a>FM \_ GETSELCOUNTLFN 訊息

由檔案管理員延伸模組所傳送，可在 [active File Manager] 視窗中取出選取的檔案數目 (目錄視窗或 [搜尋結果] 視窗) 。 計數包括具有長檔名的檔案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回選取的檔案數目。

## <a name="remarks"></a>備註

只有支援長檔名的延伸模組 (例如網路覺察的延伸模組) 應該使用此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




