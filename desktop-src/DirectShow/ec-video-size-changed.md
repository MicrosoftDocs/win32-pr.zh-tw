---
description: 原生影片大小已變更。
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: 'EC_VIDEO_SIZE_CHANGED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981633"
---
# <a name="ec_video_size_changed"></a>EC \_ 影片 \_ 大小 \_ 已變更

原生影片大小已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**DWORD**) 低序位字組指定新的寬度（以圖元為單位）。高序位字指定新的高度（以圖元為單位）。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

如果影片轉譯器偵測到原生影片大小的變更，則可能會傳送此事件。

[影片混合](video-mixing-renderer-filter-7.md)轉譯器 7 (VMR-7) 和[影片混合](video-mixing-renderer-filter-9.md)轉譯器 9 (VMR-9) 以視窗模式傳送此事件，而不是在無視窗模式或 renderless 模式下傳送。 如需 VMR 中視窗模式模式的詳細資訊，請參閱 [影片](video-rendering.md)轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




