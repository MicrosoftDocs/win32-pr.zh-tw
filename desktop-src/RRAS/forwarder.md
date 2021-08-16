---
title: 轉寄站
description: 轉寄站是路由器的核心模式元件，負責將資料從一個路由器介面轉送到其他路由器介面。
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5011d340b444c9d0be5b26ee5449f041bb7419fd4a52f8a983ce2b85d9b106f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674018"
---
# <a name="forwarder"></a>轉寄站

轉寄站是路由器的核心模式元件，負責將資料從一個路由器介面轉送到其他路由器介面。 轉寄站也會決定封包是否以本機傳遞為目的地，無論是要將它從另一個介面（或兩者）轉寄。

有兩個核心模式轉寄站：單點傳送和多播。

路由器管理員會從路由表管理員取得所有目的地的最佳路由。 這些路由會傳遞至單播轉寄站。 單播轉寄站會使用這些路由來執行單播資料的實際轉送。 如此一來，單播轉寄站會在路由表的單點傳送視圖中維護最佳路由的快取。

多播群組管理員會使用路由表的多播視圖中的資訊，將多播轉送專案新增至多播轉寄站。

 

 




