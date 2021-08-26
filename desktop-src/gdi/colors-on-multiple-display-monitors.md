---
description: 每個監視器都可以有自己的色彩深度。
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: 多顯示器顯示器上的色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd799599f3818ad002ee8a0fa1e9478f383b3052dd3a2cc3b8a40843e431b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115318"
---
# <a name="colors-on-multiple-display-monitors"></a>多顯示器顯示器上的色彩

每個監視器都可以有自己的色彩深度。 系統會在不同色彩深度的監視器之間，自動調整色彩。 一般來說，這會產生良好的結果。 不過，這不一定是最佳的作法。 若要利用不同監視的色彩功能，請參閱下面的「 [在多個顯示監視器上繪製](painting-on-multiple-display-monitors.md) 」一節。

若要判斷所有監視器是否具有相同的色彩格式，請使用 SM SAMEDISPLAYFORMAT 呼叫 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \_ 。

如果主要監視器是調色盤， [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) 和 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 的運作方式與之前相同，但會在所有監視器上運作。 此外，所有調色盤裝置的調板都會進行同步處理。 如果主要監視器未調色盤， **SelectPalette** 和 **RealizePalette** 將會在背景中選取選擇區，而調色盤裝置將不會進行同步處理。

 

 
