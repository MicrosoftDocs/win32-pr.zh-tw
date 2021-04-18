---
title: 已取代佇列的目前模型
description: 已取代佇列的目前模型
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "106965046"
---
# <a name="queued-present-model-is-being-deprecated"></a>已取代佇列的目前模型

## <a name="platforms"></a>平台

**用戶端** – Windows 8 後  
**伺服器** – Windows Server 2012 之後  


## <a name="description"></a>Description

在 Windows 8 後的 Windows 版本中，這些 Api 會傳回 E \_ >notimpl：

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

此外，此 API 只會接受 hwnd 參數的 Null 值：

-   DwmGetCompositionTimingInfo

我們將停止支援具有 hwnd！ = Null 的 DwmGetCompositionTimingInfo，並移除相關聯的功能。 如果指定 hwnd 的非 Null 值，此 API 將會傳回 E \_ INVALIDARG。

我們也鼓勵使用 DwmGetCompositionTimingInfo API，並建議開發人員切換至 DXGI 翻轉模型和相關聯的 DX 目前統計資料 API。

## <a name="manifestation"></a>表現

使用佇列的目前模型的應用程式將無法正確運作。 確切的外觀取決於特定的應用程式，但其範圍可能從不正確的呈現時機，到應用程式意外結束) 。 在實務上，如果有任何) 這類應用程式，我們就不會看到許多 (。 這是 Vista media player 使用的模型，這種模型不會用在 Windows 8 (上，也可能) 舊的 Zune 播放程式。 目前，我們沒有任何其他應用程式實際使用此模型的相關資訊。

## <a name="solution"></a>解決方法

開發人員必須使用 [DXGI 翻轉] 呈現模式，而不是從 Windows 7 開始，DX9 執行時間中提供的佇列存在 (，以及 DX10 和 DX11 相互作用執行時間的 Windows 8) 。

## <a name="tests"></a>測試

執行一般測試，以確保收件匣 Windows 元件和主要產品可在下一版 Windows 上繼續運作。

 

 




