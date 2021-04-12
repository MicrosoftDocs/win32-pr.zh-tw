---
title: 執行範例專案
description: 執行範例專案
ms.assetid: d0c32a75-4d30-408b-8da8-3917f6fd6ea4
keywords:
- Windows Media Player 線上商店，執行範例專案
- 線上商店，執行範例專案
- 類型2線上商店，執行範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 正在執行範例專案
- 範例，請輸入2個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8f42829add3ffbe5cc026f7dc2451513701fd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372388"
---
# <a name="running-the-sample-project"></a>執行範例專案

範例 COM 元件會示範 **IWMPSubscriptionServices** 方法所提供的功能，方法是在每次 Windows Media Player 呼叫其中一個方法時顯示對話方塊。 若要查看此情況，您必須先將某些內容新增至程式庫，其中包含符合您服務的 **ContentDistributor** 屬性。 請參閱 [新增 ContentDistributor 屬性](adding-the-contentdistributor-attribute.md)。 然後，使用 Windows Media Player 10 或更新版本來開啟您的線上商店、播放 premium 內容，並將您的 premium 內容複寫到裝置。 Windows Media Player 會將範例 COM 元件具現化，並在適當時呼叫方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Type 2 線上商店的外掛程式**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




