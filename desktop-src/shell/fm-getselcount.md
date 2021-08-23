---
description: 由檔案管理員延伸模組所傳送，可在 [active 檔案管理員] 視窗中取出所選檔案的計數 (目錄視窗或 [搜尋結果] 視窗) 。
title: 'FM_GETSELCOUNT 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: e309b274567ba8d7732e8db0a80bea3a001da34bd076d80c307736c4355672f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094163"
---
# <a name="fm_getselcount-message"></a>FM \_ GETSELCOUNT 訊息

由檔案管理員延伸模組所傳送，可在 [active 檔案管理員] 視窗中取出所選檔案的計數 (目錄視窗或 [搜尋結果] 視窗) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回選取的檔案數目。

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

[**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md)
</dt> </dl>

 

 




