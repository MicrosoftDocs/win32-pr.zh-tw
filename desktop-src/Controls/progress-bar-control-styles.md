---
title: '進度列控制項樣式 (CommCtrl .h) '
description: 進度列控制項支援下列控制項樣式
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1216171b116bffb962b3ebfe1a76497473cf2db2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465274"
---
# <a name="progress-bar-control-styles"></a>進度列控制項樣式

[進度](progress-bar-control.md)列控制項支援下列控制項樣式：




| 常數 | 描述 | 
|----------|-------------|
| <span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl><dt><strong>PBS_MARQUEE</strong></dt></dl> | <a href="common-control-versions.md">6.0 版</a> 或更新版本。 進度指示器的大小不會增加，而是沿著橫條的長度重複移動，表示活動，而不指定進度的比例。 <br /><blockquote>[!Note]<br />Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 或更新版本中。 若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</blockquote><br /> | 
| <span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl><dt><strong>PBS_SMOOTH</strong></dt></dl> | <a href="common-control-versions.md">4.70 版</a> 或更新版本。 進度列會在平滑捲軸中顯示進度狀態，而不是以預設分割的橫條圖顯示。 <br /><blockquote>[!Note]<br />只有 Windows 傳統主題才支援這個樣式。 所有其他主題都會覆寫這個樣式。</blockquote><br /> | 
| <span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl><dt><strong>PBS_SMOOTHREVERSE</strong></dt></dl> | <a href="common-control-versions.md">6.0 版</a>或更新版本，以及<strong>Windows Vista。</strong> 決定當 (從較高的值移至較低的值) 時，進度列應使用的動畫行為。 如果設定了此值，則會發生「平滑」轉換，否則控制項將「跳至」至較低的值。<br /> | 
| <span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl><dt><strong>PBS_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">4.70 版</a> 或更新版本。 進度列會從下到上垂直顯示進度狀態。<br /> | 




## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)、 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)或 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)，以與其他通用控制項相同的方式設定進度列樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

