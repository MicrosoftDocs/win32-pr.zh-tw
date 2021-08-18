---
description: 所有監視器的周框都是虛擬螢幕。 桌面涵蓋了虛擬畫面，而不是單一監視器。 下圖顯示三個監視器的可能相片順序。
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: 虛擬畫面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5516ef0cb5d99124200ab7810e484ea79027cf832a0e8da74833bf709ce5cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037516"
---
# <a name="the-virtual-screen"></a>虛擬畫面

所有監視器的周框都是 *虛擬螢幕*。 桌面涵蓋了虛擬畫面，而不是單一監視器。 下圖顯示三個監視器的可能相片順序。

![顯示三個方塊的圖例，代表在代表虛擬畫面的方塊中排列的監視器](images/multimon-1.png)

*主要監視器* 包含來源 (0、0) 。 這是為了與預期監視器具有來源的現有應用程式相容。 不過，主要監視器不一定要位於虛擬螢幕的左上方。 在 [圖 1] 中，它位於中央附近。 當主要監視器不在虛擬畫面的左上方時，虛擬畫面的元件會有負面的座標。 因為監視的排列是由使用者設定，所以所有應用程式都應該設計為使用負座標。 如需詳細資訊，請參閱 [舊版程式的多個監視器考慮](multiple-monitor-considerations-for-older-programs.md)。

虛擬螢幕的座標會以帶正負號的16位值表示，因為許多現有的訊息中包含16位值。 因此，虛擬畫面的界限如下：

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



