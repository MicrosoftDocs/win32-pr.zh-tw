---
title: 已取代佇列的目前模型
description: 已取代佇列的目前模型
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cb1d4d07a824c2c6f9d0136259aec98b89c53e1320ceb6402241f881e312fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211343"
---
# <a name="queued-present-model-is-being-deprecated"></a>已取代佇列的目前模型

## <a name="platforms"></a>平台

**用戶端**– Windows 8 後  
**伺服器**– Windows Server 2012 後  


## <a name="description"></a>Description

在 Windows 8 之後的 Windows 版本中，這些 api 會傳回 E \_ >notimpl：

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

此外，此 API 只會接受 hwnd 參數的 Null 值：

-   DwmGetCompositionTimingInfo

我們將停止支援具有 hwnd！ = Null 的 DwmGetCompositionTimingInfo，並移除相關聯的功能。 如果指定 hwnd 的非 Null 值，此 API 將會傳回 E \_ INVALIDARG。

我們也鼓勵使用 DwmGetCompositionTimingInfo API，並建議開發人員切換至 DXGI 翻轉模型和相關聯的 DX 目前統計資料 API。

## <a name="manifestation"></a>表現

使用佇列的目前模型的應用程式將無法正確運作。 確切的外觀取決於特定的應用程式，但其範圍可能從不正確的呈現時機，到應用程式意外結束) 。 在實務上，如果有任何) 這類應用程式，我們就不會看到許多 (。 這是 Vista media player 所使用的模型，這種模型不會用在 Windows 8 (，而且可能是舊的 Zune 播放程式) 。 目前，我們沒有任何其他應用程式實際使用此模型的相關資訊。

## <a name="solution"></a>解決方案

開發人員必須使用 [DXGI 翻轉] 呈現模式，而不是 DX9 執行時間中提供的佇列 (，因為 Windows 7 和 Windows 8) 中的 DX10 和 dx11 相互作用執行時間。

## <a name="tests"></a>測試

執行一般測試，以確保收件匣 Windows 元件和主要產品可在下一版的 Windows 上繼續運作。

 

 




