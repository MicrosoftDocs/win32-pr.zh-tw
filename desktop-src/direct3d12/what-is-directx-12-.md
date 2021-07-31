---
title: 什麼是 Direct3D 12
description: DirectX 12 引進了下一版的 Direct3D;以 DirectX 為核心的3D 圖形 API。
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: f82b01ba33cfa6660f266a481b2eaaab20ade236
ms.sourcegitcommit: 60ff57d8cf94ae7a47c6046ad49f7c7256a7edb6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/31/2021
ms.locfileid: "115006793"
---
# <a name="what-is-direct3d-12"></a>什麼是 Direct3D 12？

DirectX 12 引進了下一版的 Direct3D，也就是 &mdash; directx 核心的3d 圖形 API。 Direct3D 12 比之前的版本更快且更有效率。 Direct3D 12 提供更豐富的場景、更多物件、更複雜的效果，以及新式 GPU 硬體的完整使用率。

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>Direct3D 12 的速度更快且更有效率嗎？

Direct3D 12 的獨特之處在于，它提供比舊版更低的硬體抽象層，可讓您大幅改善標題 (或其他應用程式) 的多重核心 CPU 調整。 針對一件事，使用 Direct3D 12 時，您的標題會負責自己的 [記憶體管理](memory-management.md)。 此外，藉由使用 Direct3D 12，您的標題和應用程式可以透過 [命令佇列和清單](command-queues-and-command-lists.md)、 [描述項資料表](descriptor-tables.md)和簡潔的 [管線狀態物件](managing-graphics-pipeline-state-in-direct3d-12.md)等功能，從降低 GPU 額外負荷獲益。

Direct3D 12 和 Direct3D 11.3 引進一組適用于轉譯管線的新功能。

- [保守的光柵](../direct3d11/conservative-rasterization.md) 化，以啟用可靠的點擊偵測。
- [磁片](../direct3d11/volume-tiled-resources.md) 區並排顯示的資源，可讓您將串流處理的三維資源視為全部都在視訊記憶體中。
- 以轉譯器為[排序的視圖](../direct3d11/rasterizer-order-views.md)，可啟用可靠的透明呈現。
- 設定著色器內的樣板參考，以啟用特殊遮蔽和其他效果。
- 改良的材質對應和具類型的未排序存取視圖 (UAV) 載入。

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>我應該在 Direct3D 12 中投資多深？

相較于 Direct3D 11) ，Direct3D 12 為圖形開發人員提供四個主要優點 (。

- 大幅降低 CPU 額外負荷。
- 大幅降低耗電量。
- 最高 (大約) 20% 的 GPU 效率改進。
- Windows 10 裝置的跨平臺開發 (電腦、平板電腦、主控台、行動) 。

Direct3D 12 的設計目的是要讓先進的圖形程式設計人員使用。 它會呼叫大量的圖形專長，以及高度微調。 Direct3D 12 的設計目的是充分利用多重執行緒、審慎的 CPU/GPU 同步處理，以及將資源從一個用途轉換和重複使用到另一個用途。 這些都是需要大量記憶體層級程式設計技能的技術。

Direct3D 12 的另一個優點是它的小型 API 足跡。 大約200個函式;而這第三個動作的第三個則是全部繁重的工作。 這表示您（圖形開發人員）應該能夠 &mdash; 事先教育並主控 &mdash; 完整的 api 設定，而不需要記住太多 api 名稱。

Direct3d 11 會持續成為 Direct3D 12 的可行選項。 Direct3d 12 的許多新轉譯功能都可在 [direct3d 11.3](../direct3d11/direct3d-11-3-features.md)中使用。 Direct3D 11.3 是低層級的圖形引擎 API;而 Direct3D 12 甚至更深入。

您的開發小組至少有兩種方法可以處理 Direct3D 12 的標題。

### <a name="use-direct3d-12-exclusively"></a>以獨佔方式使用 Direct3D 12

對於充分利用 Direct3D 12 所有優點的專案，您應該從頭開始開發高度自訂的 Direct3D 12 引擎。

如果您是圖形開發人員，請瞭解如何使用和重複使用標題中的資源，而且您可以藉由最小化上傳和複製來充分利用，然後您可以為這些標題開發和自訂高效率的引擎。 效能的改進可能很可觀、釋出 CPU 時間以增加繪製呼叫的數目，以及新增更多叢集至您的圖形。

程式設計的投資很重要，因此您應該考慮從一開始就開始進行專案的調試和檢測。 執行緒、同步處理和其他計時 bug 可能很困難。

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>使用 Direct3D 12 搭配 Direct3D 11

較短期的方法是解決 Direct3D 11 標題中的已知瓶頸。 您可以使用 [Direct3D 12 interop 及/或 D3D11On12](direct3d-12-interop.md) 技術來解決這些情況，讓兩個 API 版本能夠一起運作。 這種方法可將現有 Direct3D 11 圖形引擎所需的變更降至最低。 不過，效能提升的範圍僅限於 Direct3D 12 程式碼所能解決的瓶頸。

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Microsoft DirectX 12 (和圖形教育) 影片

[對圖形開發人員的增強教育](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)。 這些影片涵蓋簡報模式、移植至 DirectX 12、保守的點陣化、圖形工具、角度、Win2D 和事件（例如 GDC、組建等等）等主題。 技術 DirectX 12 內容前面會加上 *directx 12*。 從這裡開始，直接從 Direct3D 12 功能小組學習秘訣和訣竅。 我們想要協助您使用我們最新的版本和工具，讓您的遊戲發揮最大效果！

## <a name="conclusion"></a>結論

Direct3D 12 的功能全都是大幅圖形引擎的效能。 簡易開發、高階結構和編譯器支援已相應放大以啟用此項。 驅動程式支援和輕鬆的偵錯工具與 Direct3D 11 保持等同。

Direct3D 12 是新領域。 正在等待好學專家提出和探索的領域。
