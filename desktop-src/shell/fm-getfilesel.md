---
description: 由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。
title: 'FM_GETFILESEL 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: a801b22fd23b4a67eaf01efbbef574e24a74a2e1304f3a65678c4197517a4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094183"
---
# <a name="fm_getfilesel-message"></a>FM \_ GETFILESEL 訊息

由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。

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

延伸模組可以使用 [**FM \_ GETSELCOUNT**](fm-getselcount.md) 訊息來取出所選檔案的計數。

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

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md)
</dt> </dl>

 

 




