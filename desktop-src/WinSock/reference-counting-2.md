---
description: 進程可能會在重複的通訊端上呼叫 WSPCloseSocket，而描述項將會解除配置。 不過，基礎通訊端會保持開啟，直到在最後一個描述項上呼叫 WSPCloseSocket 為止。
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: 參考計數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8cd281363636cc2022725b4921d3b2d2b300e7262173e157a2be1610f6af0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996658"
---
# <a name="reference-counting"></a>參考計數

進程可能會在重複的通訊端上呼叫 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) ，而描述項將會解除配置。 不過，基礎通訊端會保持開啟，直到在最後一個描述項上呼叫 **WSPCloseSocket** 為止。

 

 
