---
description: 關於影片捕獲裝置
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: 關於影片捕獲裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687864"
---
# <a name="about-video-capture-devices"></a>關於影片捕獲裝置

大部分新的影片捕獲裝置都會使用 Windows Driver Model (WDM) 驅動程式。 在 WDM 架構中，Microsoft 提供一組與硬體無關的驅動程式，稱為類別驅動程式，硬體廠商則提供硬體特定的 minidrivers。 迷你驅動程式會實作用於裝置的任何函式;針對大部分的函式，迷你驅動程式會呼叫 Microsoft class 驅動程式。

在 DirectShow 篩選圖形中，任何 WDM 捕獲裝置都會顯示為 [Wdm 影片捕獲](wdm-video-capture-filter.md) 篩選器。 WDM 影片捕獲篩選器會根據驅動程式的特性來設定本身。 它會顯示在驅動程式所提供的名稱底下，在圖形中的任何位置都不會看到名為「WDM 影片捕獲篩選器」的篩選。

某些較舊的捕獲裝置仍會使用適用于 Windows (VFW) 驅動程式的影片。 雖然這些驅動程式現在已過時，但可透過 [VFW Capture](vfw-capture-filter.md) 篩選器在 DirectShow 中受到支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectShow 中的影片捕獲](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



