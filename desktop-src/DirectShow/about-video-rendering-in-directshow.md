---
description: 關於 DirectShow 中的影片轉譯
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: 關於 DirectShow 中的影片轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846747"
---
# <a name="about-video-rendering-in-directshow"></a>關於 DirectShow 中的影片轉譯

DirectShow 提供數個轉譯影片的篩選：

-   [影片](video-renderer-filter.md) 轉譯器篩選。 此篩選器適用于所有支援 DirectX 的平臺，而且沒有特定的系統需求。 影片轉譯器會盡可能使用 DirectDraw 來呈現影片;否則，它會使用 GDI。 此篩選器是 Windows XP 之前平臺上的預設影片轉譯器。
-   [影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) 。 VMR-7 可在 Windows XP 上取得，其為預設的影片轉譯器。 VMR-7 一律會使用 DirectDraw 7 來呈現。 它提供了許多較舊的影片轉譯器篩選器中未提供的強大功能，包括外掛程式模型，其中應用程式會控制用來轉譯的 DirectDraw 表面。
-   [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 。 VMR-9 是較新版本的視頻混合轉譯器，它會使用 Direct3D 9 來呈現。 它適用于所有支援 DirectX 的平臺。 不過，它並不是預設轉譯器，因為它的系統需求比影片轉譯器篩選器更高。
-   覆迭 [混音](overlay-mixer-filter.md) 器篩選器是專門針對 DVD 播放和廣播影片所設計。 它也支援 (VPEs) 的影片埠擴充功能，讓它能夠使用硬體 MPEG-2 解碼器或類比電視調諧器，直接將影片傳送至圖形配接器。
-   從 Windows Vista 開始，可以使用 (EVR) 篩選器的 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器。 相較于先前的影片轉譯器，它提供改良的影片效能，特別是在啟用 Windows Vista 桌面電腦群組合的情況下。

一般來說，對於以 Windows Vista 或更新版本為目標的應用程式而言，EVR 是慣用的，而在舊版 Windows 上執行的應用程式則偏好 VMR-9。 如需使用 VMR-7 和 VMR-9 篩選器的詳細資訊，請參閱 [使用影片混合](using-the-video-mixing-renderer.md)轉譯器。

視窗模式和無視窗模式

DirectShow 影片轉譯器可以在 *視窗* 模式或 *無視窗* 模式下運作。

-   在視窗模式中，轉譯器會建立自己的視窗來顯示影片。 通常您會將此視窗設為應用程式視窗的子系。 如需詳細資訊，請參閱 [使用視窗模式](using-windowed-mode.md)。
-   在無視窗模式中，轉譯器會將影片直接繪製到應用程式視窗。 它不會建立自己的視窗。 如需此模式的詳細資訊，請參閱 [使用無視窗模式](using-windowless-mode.md)。

影片轉譯器篩選僅支援視窗模式。 VMR-7 和 VMR-9 篩選器都支援這兩種模式。 它們預設為視窗模式，以提供回溯相容性，但最好是無視窗模式。 EVR 只支援無視窗模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片轉譯](video-rendering.md)
</dt> </dl>

 

 



