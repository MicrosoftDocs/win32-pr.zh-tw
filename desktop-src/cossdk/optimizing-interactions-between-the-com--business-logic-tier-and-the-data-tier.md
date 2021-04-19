---
description: 資料層通常會包含靜態資訊&\# 郵件; 保存在永久性媒體上的資訊。
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: 優化 COM + 商務邏輯與資料之間的呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972554"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>優化 COM + 商務邏輯層與資料層之間的互動

資料層通常會包含靜態資訊，也就是保存在永久性媒體上的資訊。 因為這一層包含大部分是靜態的資訊，所以需要徹底分析潛在的瓶頸。 除了明顯的連接瓶頸可能性，作用點可能是經常存取的記錄、無效率的資料存取方法，以及協調存取舊版系統的需求所造成。

## <a name="connecting-to-the-data-tier"></a>連接到資料層

在設計 COM + 應用程式的資料層時，有兩個考慮扮演重要角色：連接共用和 [Com + 及時 (JIT) 啟用](com--just-in-time-activation.md)，以及使用 dsn。 建立資料層連接的元件應該使用元件上設定的 [Com + 物件](com--object-pooling.md) 共用。

建立 Dsn 時，請使用在元件上指定的物件指定函式字串，而不是建立 File DSN。 檔案 Dsn 比使用物件的函式字串的連接慢。 可以在元件屬性工作表上指定物件的函式字串。 如需詳細資訊，請參閱 [Com + 物件](com--object-constructor-strings.md)的函式字串。

如果您使用元件來存取 SQL Server 資料庫，請使用 COM + 物件共用，而不是 SQL 連接共用。

如果您的元件使用 ADO 提取多個記錄集，請建立元件的多個連接。 當 ADO 抓取多個記錄集時，如果您未建立，就會在背景中建立多個連接。 如果您建立它們，您可以將它們集區化，並對所使用的連線數目有更大的控制權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 COM + 商務邏輯層和展示層之間的互動優化](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



