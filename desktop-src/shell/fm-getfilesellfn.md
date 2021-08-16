---
description: 由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。 選取的檔案可以有較長的檔案名。
title: 'FM_GETFILESELLFN 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: 2074fb1e631edf1795b8f0d15ea9f0d40e90556d527899873ef88195c2367576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860765"
---
# <a name="fm_getfilesellfn-message"></a>FM \_ GETFILESELLFN 訊息

由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。 選取的檔案可以有較長的檔案名。

## <a name="parameters"></a>參數

<dl> <dt>

*index* 
</dt> <dd>

要抓取之所選取檔案的以零為起始的索引。

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

[**FMS \_ GETFILESEL**](fms-getfilesel.md)結構的位址，此結構會接收選取專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回所選取檔案的以零為基底的索引。

## <a name="remarks"></a>備註

只有支援長檔名的延伸模組 (例如網路覺察的延伸模組) 應該使用此訊息。

延伸模組可以使用 [**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) 訊息來取出所選檔案的計數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




