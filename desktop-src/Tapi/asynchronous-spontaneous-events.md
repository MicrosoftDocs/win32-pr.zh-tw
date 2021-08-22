---
description: 除了上述的非同步事件之外，還有另一個類別。
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: 非同步自發事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785ed97e6538b1baff9af13e64791a094d872e540fc088b74820119629d08b4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871903"
---
# <a name="asynchronous-spontaneous-events"></a>非同步自發事件

除了上述的非同步事件之外，還有另一個類別。 這些事件是「自發」的意義，因為它們不是對應要求的直接結果。 在這種情況下，偵測到傳入的呼叫抵達時，或從「響鈴」進入「正在接聽」狀態時，就會偵測到這些事件。 當 TAPI 首次初始化與特定裝置的 TSPI 互動時，它會傳遞回呼程式的指標，以針對報告這類自發事件進行呼叫。 除了這個程式指標，也是服務提供者以其中一個實際參數的形式包含在回呼中的裝置控制碼。

 

 



