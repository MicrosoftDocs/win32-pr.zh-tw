---
title: 測量視頻品質
description: 測量視頻品質
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021374"
---
# <a name="measuring-video-quality"></a>測量視頻品質

測量視頻品質的其中一種方式是限制在捕獲作業期間卸載的已捨棄框架數目。 串流處理捕獲完成時，會將品質值與卸載的框架比例與總畫面格的比率進行比較。 如果捨棄的框架百分比大於 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **wPercentDropForError** 成員值，AVICap 會將錯誤訊息傳送至錯誤回呼函式（如果已安裝）。

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息] (或 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前已卸載框架的限制 (以百分比) 表示。 您可以設定新的限制，方法是將百分比指定為 **CAPTUREPARMS** 結構的 **wPercentDropForError** 成員值，然後使用 [ [**WM \_ CAP \_ set \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的結構傳送至 [捕獲] 視窗。 **WPercentDropForError** 的預設值為10%。

 

 




