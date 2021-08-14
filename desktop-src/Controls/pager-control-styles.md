---
title: " (CommCtrl 的呼機控制項樣式) "
description: 此區段會列出建立呼機控制項時使用的視窗樣式。
ms.assetid: 619fd8cc-e231-41af-8744-a29d14f2c6f8
topic_type:
- apiref
api_name:
- PGS_AUTOSCROLL
- PGS_DRAGNDROP
- PGS_HORZ
- PGS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b97c7df35fc1883274e42fe54c9ff62415da5dca7e2f020b9371ea873fecc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170215"
---
# <a name="pager-control-styles"></a>呼機控制項樣式

此區段會列出建立呼機控制項時使用的視窗樣式。



| 常數                                                                                                                                                         | 描述                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGS_AUTOSCROLL"></span><span id="pgs_autoscroll"></span><dl> <dt>**PG \_ AUTOSCROLL**</dt> </dl> | 當使用者將滑鼠停留在其中一個捲軸按鈕上方時，就會滾動頁控制項。<br/>                                                                                                                     |
| <span id="PGS_DRAGNDROP"></span><span id="pgs_dragndrop"></span><dl> <dt>**PG \_ DRAGNDROP**</dt> </dl>    | 包含的視窗可以是拖放目標。 如果從分頁外部將某個專案拖曳至其中一個捲軸按鈕，則會自動滾動頁控制項。<br/>                                     |
| <span id="PGS_HORZ"></span><span id="pgs_horz"></span><dl> <dt>**PG \_ HORZ**</dt> </dl>                   | 建立可水準滾動的呼機控制項。 這個樣式和 **pg \_ 垂直** 樣式是互斥的，無法合併。<br/>                                                                 |
| <span id="PGS_VERT"></span><span id="pgs_vert"></span><dl> <dt>**PG \_ 垂直**</dt> </dl>                   | 建立可以垂直捲動的分頁控制項。 如果未指定方向樣式，則這是預設方向。 這個樣式和 **pg \_ HORZ** 樣式互斥，而且無法合併。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





