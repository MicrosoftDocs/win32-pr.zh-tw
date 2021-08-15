---
title: 精確的 Capture 控制項
description: 精確的 Capture 控制項
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- AVICap 回呼函式，精確的 capture 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365482f5f6309f9642aa5c8b497b58a1d9416e398e5c3624191d777e006b23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372658"
---
# <a name="precise-capture-control"></a>精確的 Capture 控制項

捕捉視窗可以提供 capture 控制項回呼函式，並精確地控制串流處理的開始和結束時間。 從 capture 驅動程式傳送到回呼程式的第一個訊息會將 *nState* 參數設定為 \_ 在配置所有緩衝區後 CONTROLCALLBACK 預先設定，並完成所有其他的捕獲準備工作。 此訊息可讓應用程式預先擁有影片來源的能力。  (回呼函式會將 *nState* 指定為其第二個參數。 ) 回呼函式，則會在確切的時刻記錄開始時傳回。 回呼函式中 **TRUE** 的傳回值會繼續捕捉。 **FALSE** 中止捕捉的傳回值。 一旦開始 capture，會經常呼叫回呼函式，並將 *nState* 設定為 CONTROLCALLBACK capture， \_ 以允許應用程式藉由傳回 **FALSE** 來結束捕捉。

 

 




