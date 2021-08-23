---
description: 以下是筆觸常數。
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: '筆觸常數 (Tabflicks .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e927d0715c9f34e7e1db979c32545a0d8c8efad18186192a751f2cdbed13172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092645"
---
# <a name="flicks-constants"></a>筆觸常數

以下是筆觸常數。



| 常數/值                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**筆鋒 \_WM \_ 處理的 \_ 遮罩**</dt> <dt>0x1</dt> </dl> | 處理 [**WM \_ TABLET \_ 筆鋒訊息**](wm-tablet-flick-message.md) 訊息之後要傳回的值。 如果傳回了 [筆觸 **\_ WM \_ 處理的 \_ 遮罩** ]，就不會進行任何進一步的動作。 否則，Windows 會傳送後續通知，例如 [**wm \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand)、 [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)或 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)，取決於與筆觸相關聯的動作。 <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**NUM \_筆鋒 \_ 方向**</dt> <dt>8</dt> </dl>       | 在 [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) 列舉中定義的方向數目。<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Tabflicks。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FLICKDIRECTION 列舉**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**WM \_ TABLET \_ 筆鋒訊息**](wm-tablet-flick-message.md)
</dt> <dt>

[筆觸手勢](flicks-gestures.md)
</dt> <dt>

[回應觸控筆觸](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

