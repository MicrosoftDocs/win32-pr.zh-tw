---
title: 使用 HTMLView 搭配線上商店
description: 使用 HTMLView 搭配線上商店
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player 線上商店，HTMLView
- 線上商店、HTMLView
- 輸入1個線上商店，HTMLView
- 輸入2個線上商店，HTMLView
- HTMLView，線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d5e89e2d0eaff2d51f8fa03281bf1ce85878b1863df619c28cdd228beb1eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465888"
---
# <a name="using-htmlview-with-online-stores"></a>使用 HTMLView 搭配線上商店

Windows Media Player 會提示使用者顯示 **目前播放** 中 HTMLView 內容的許可權。 線上商店可以停用此提示，方法是在 ServiceInfo 檔的 **HTMLView** 元素中指定基底 URL 值。 當 Windows Media Player 開啟播放清單來指定要顯示的 HTMLView 內容時，播放程式會比較目前作用中線上商店的 ServiceInfo 檔中的基底 url 與 HTMLView 內容的基底 url。 如果相符，Windows Media Player 會顯示 HTMLView 內容而不提示使用者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**HTMLView 元素**](htmlview-element.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




