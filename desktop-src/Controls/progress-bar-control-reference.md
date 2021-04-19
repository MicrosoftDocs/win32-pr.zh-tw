---
title: 進度列
description: 本章節包含與進度列控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b99a31bbbd3b80de0d528d5232c79c28af1e1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967611"
---
# <a name="progress-bar"></a>進度列

本章節包含與進度列控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                            | 目錄                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [進度列控制項](progress-bar-control.md) | 進度列是一種視窗，可讓應用程式用來指出冗長作業的進度。<br/> |



 

### <a name="messages"></a>訊息



| 主題                                       | 目錄                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBM \_ DELTAPOS**](pbm-deltapos.md)       | 依指定的遞增量將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。 <br/>                                                                                                                                 |
| [**PBM \_ GETBARCOLOR**](pbm-getbarcolor.md) | 取得進度列的色彩。<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETBKCOLOR**](pbm-getbkcolor.md)   | 取得進度列的背景色彩。<br/>                                                                                                                                                                                                             |
| [**PBM \_ GETPOS**](pbm-getpos.md)           | 抓取進度列的目前位置。 <br/>                                                                                                                                                                                                       |
| [**PBM \_ GETRANGE**](pbm-getrange.md)       | 抓取指定進度列控制項目前最高和最低限制的相關資訊。 <br/>                                                                                                                                                              |
| [**PBM \_ >GETSTATE**](pbm-getstate.md)       | 取得進度列的狀態。<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETSTEP**](pbm-getstep.md)         | 捕獲進度列的步驟增量。 步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。<br/>                                               |
| [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) | 在進度列控制項中設定進度指標列的色彩。 <br/>                                                                                                                                                                                 |
| [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md)   | 設定進度列中的背景色彩。 <br/>                                                                                                                                                                                                            |
| [**PBM \_ SETMARQUEE**](pbm-setmarquee.md)   | 設定捲軸模式的進度列。 這會使進度列像字幕一樣移動。<br/>                                                                                                                                                                |
| [**PBM \_ SETPOS**](pbm-setpos.md)           | 設定進度列的目前位置，並重新繪製橫條以反映新的位置。 <br/>                                                                                                                                                             |
| [**PBM \_ SETRANGE**](pbm-setrange.md)       | 設定進度列的最小值和最大值，並重新繪製橫條以反映新的範圍。<br/>                                                                                                                                                       |
| [**PBM \_ SETRANGE32**](pbm-setrange32.md)   | 將進度列控制項的範圍設定為32位值。 <br/>                                                                                                                                                                                               |
| [**PBM \_ SETSTATE**](pbm-setstate.md)       | 設定進度列的狀態。<br/>                                                                                                                                                                                                                        |
| [**PBM \_ SETSTEP**](pbm-setstep.md)         | 指定進度列的步驟增量。 步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。 依預設，步驟遞增會設定為10。 <br/> |
| [**PBM \_ STEPIT**](pbm-stepit.md)           | 將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。 應用程式會藉由傳送 [**PBM \_ SETSTEP**](pbm-setstep.md) 訊息來設定步驟增量。 <br/>                                |



 

### <a name="structures"></a>結構



| 主題                      | 目錄                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | 包含進度列控制項的最高和最低限制的相關資訊。 此結構會與 [**PBM \_ GETRANGE**](pbm-getrange.md) 訊息搭配使用。 <br/> |



 

### <a name="constants"></a>常數



| 主題                                                          | 目錄                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [進度列控制項樣式](progress-bar-control-styles.md) | **進度** 列控制項支援下列控制項樣式：<br/> |



 

 

 





