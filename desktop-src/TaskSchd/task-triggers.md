---
title: 工作觸發程式
description: 觸發程序就是一組條件，當符合那些條件時，就會啟動工作執行。
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- 建立觸發程式工作排程器
- 觸發程式工作排程器
- 觸發程式工作排程器，說明
- 以時間為基礎的觸發程式工作排程器
- 以事件為基礎的觸發程式工作排程器
- 以事件為基礎的觸發程式工作排程器
- 以時間為基礎的觸發程式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183149"
---
# <a name="task-triggers"></a>工作觸發程式

觸發程序就是一組條件，當符合那些條件時，就會啟動工作執行。 工作排程器提供以時間為基礎和以事件為基礎的觸發程式，可以用數種不同的方式來啟動工作。 一或多個觸發程式可以啟動指定的工作。 工作最多可有48個觸發程式。

## <a name="time-based-triggers"></a>以時間為基礎的觸發程式

以時間為基礎的觸發程式會在指定的時間啟動工作。 這包括每日、每週、每月或每月星期幾排程，在特定時間啟動一次工作，或多次啟動工作。

## <a name="event-based-triggers"></a>以事件為基礎的觸發程式

以事件為基礎的觸發程序可啟動工作來回應特定的系統事件。 例如，您可以設定以事件為基礎的觸發程式，以便在系統啟動時、使用者登入本機電腦時，或系統變成閒置時啟動工作。

## <a name="multiple-triggers"></a>多重觸發程序

每項工作都可以透過一個或多個觸發程式來啟動，讓工作以任何數目的方式啟動。 不過，在工作排程器1.0 和工作排程器2.0 中，會以不同的方式來執行多個觸發程式。

在工作排程器2.0 中，每個觸發程式都是由透過觸發程式集合與工作相關聯的個別觸發程式 API 所定義。

在工作排程器1.0 中，可以將多個觸發程式視為排程，也就是工作開始的一組時間。 在此情況下，排程是一組時間 (由與工作專案所執行之工作專案) 相關聯之所有觸發程式的聯集來指定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[重複工作](repeating-a-task.md)
</dt> <dt>

[觸發程式類型](trigger-types.md)
</dt> <dt>

[觸發程式介面](trigger-interfaces.md)
</dt> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> </dl>

 

 




