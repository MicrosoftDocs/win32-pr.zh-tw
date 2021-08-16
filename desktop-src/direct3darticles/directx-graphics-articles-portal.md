---
title: DirectX 圖形文章
description: DirectX 圖形文章
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5562b4b7dafc899d1c6a827cfd2e240a20013be7a31f225cdd41893d967748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095498"
---
# <a name="directx-graphics-articles"></a>DirectX 圖形文章

## <a name="purpose"></a>目的

本章節包含的技術文章會說明變形和 Windows 7 新增的翻轉模式支援，以及其在 Direct3D 9Ex 和桌面視窗管理員中的目前相關統計資料。 本節也包含有關 Windows 圖形 api、將 direct3d 9 api 移植到 Microsoft DirectX Graphic Infrastructure (DXGI) api 以及如何部署 Direct3D 11 的技術文章。

如需 Direct3D 的詳細資訊，請參閱 [direct3d](/windows/desktop/direct3d)。

## <a name="developer-audience"></a>開發人員對象

這些技術文章適用于 DirectX 圖形應用程式開發人員。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [Windows 7 的平臺更新](platform-update-for-windows-7.md) | 描述 Windows 8 圖形堆疊的哪些元件可供使用，以及透過[Windows 7 的平臺更新](https://support.microsoft.com/kb/2670838)的範圍。 |
| [Direct3D 9Ex 改進](direct3d-9ex-improvements.md) | 描述 Windows 7 的新加入的翻轉模式支援，以及其在 Direct3D 9Ex 和桌面視窗管理員中的現有統計資料。 目標應用程式包括影片或以畫面播放速率為基礎的簡報應用程式。 使用 Direct3D 9Ex Flip 模式的應用程式，現在可以在啟用 DWM 時減少系統資源載入。 呈現與翻轉模式相關聯的統計資料增強功能，可讓 Direct3D 9Ex 應用程式藉由提供即時意見反應和修正機制，更有效地控制簡報的速率。 內含範例資源的詳細說明和指標。 |
| [Windows 圖形 API 之間共用的介面](surface-sharing-between-windows-graphics-apis.md) | 提供在 Windows 圖形 api （包括 direct3d 11、Direct2D、direct3d 10 和 direct3d 9Ex）之間使用介面共用的互通性技術總覽。 如果您已經瞭解這些 api，這份檔可協助您使用多個 api，在針對 Windows 7 或 Windows Vista 作業系統設計的應用程式中，轉譯成相同的介面。 本主題也提供最佳做法指導方針和其他資源的指標。 |
| [變形指南](directx-warp.md) | 提供 Windows 先進的點陣化平臺 (變形) （高速軟體轉譯器）的指南。 |
| [Windows 中的圖形 Api](graphics-apis-in-windows-vista.md) | 討論 Windows 圖形功能和 api。 |
| [適用于遊戲開發人員的 Direct3D 11 部署](direct3d11-deployment.md) | 說明如何將 Direct3D 11 元件部署到系統上。 |
| [DirectX Graphic Infrastructure (DXGI) ：最佳作法](dxgi-best-practices.md) | 討論將 Direct3D 9 Api 移植至 DXGI Api 的相關問題，以及各種版本之 DXGI 的功能。 |
| [使用 DirectX 搭配高動態範圍顯示和進階色彩](high-dynamic-range.md) | 本主題提供使用 Windows 10 advanced color support 將高動態範圍 Direct3D 11 和 Direct3D 12 內容轉譯為 HDR10 顯示的技術總覽。 |
