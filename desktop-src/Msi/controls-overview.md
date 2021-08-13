---
description: Windows安裝程式會執行封裝作者可放置於對話方塊上的一些標準控制項。 不過，並非所有標準的 Microsoft Windows 控制項都可使用，而且無法建立自訂控制項以搭配安裝程式 UI 使用。
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: 控制項概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee9d03f0f21f9cc0611a1fae4831b6ccbbda9f40eda873cdf4c26b259ec43f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638520"
---
# <a name="controls-overview"></a>控制項概觀

Windows安裝程式會執行封裝作者可放置於對話方塊上的一些標準控制項。 不過，並非所有標準的 Microsoft Windows 控制項都可使用，而且無法建立自訂控制項以搭配安裝程式 UI 使用。

在安裝程式的對話方塊中建立控制項的方式，類似于使用 Microsoft Windows 使用者介面 API 以程式設計方式建立對話方塊的方式。 控制項是從控制項資料表中記錄的範本建立。 此範本稍有不同，因為它包含控制項顯示所在對話方塊的唯一名稱。

在 Microsoft Windows 使用者介面 API 中，藉由建立回呼函式來處理控制項張貼的訊息，來完成使用者互動。 此外，大部分的 Microsoft Windows 控制項都能接收訊息，例如[SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)函式所傳送的訊息。

使用者與控制項之間的通訊是透過使用控制項，在安裝程式中[完成。](controlevent-overview.md) 不過，有一組有限的控制項，專屬於 Windows Installer 中有限控制項集合中的每個控制項。 控制項可以張貼一個以上的 ControlEvent，而且可能會收到多個 ControlEvent。

控制項可以透過使用 ControlEvent 資料表來發行特定的事件。 控制項可以透過使用 [EventMapping 資料表](eventmapping-table.md)來接收事件。

Windows安裝程式在執行某些動作時，也會在執行過程中發行工作，而在 EventMapping 資料表中訂閱這些事件的控制項則會接收這些動作。

 

 
