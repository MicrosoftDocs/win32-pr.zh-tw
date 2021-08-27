---
title: 'EM_GETSTORYTYPE 訊息 (Richedit .h) '
description: 取得案例類型。
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- EM_GETSTORYTYPE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e6d501fffca857e1e283f2678c1b42e5d3d12e587e51a3a58585041489f8b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048778"
---
# <a name="em_getstorytype-message"></a>EM \_ GETSTORYTYPE 訊息

取得案例類型。


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

故事索引。

</dd> <dt>

*lParam* 
</dt> <dd>

保護必須是0。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回案例類型（可以是用戶端定義的自訂值），或下列其中一個值：

<dl> <dt>

**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETSTORYTYPE**](em-setstorytype.md)
</dt> <dt>

[**ITextStoryRanges：： Item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





