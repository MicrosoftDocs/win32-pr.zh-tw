---
description: 開始使用 DirectX 圖形
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: 開始使用 DirectX 圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c5e8cca9f0cea4c1c5e484ba330c7c108cad40
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117586"
---
# <a name="getting-started-with-directx-graphics"></a>開始使用 DirectX 圖形

Microsoft DirectX 圖形提供一組 Api，可讓您用來建立遊戲和其他高效能的多媒體應用程式。 DirectX 圖形包含高效能的2D 和3D 圖形支援。

若是立體圖形，請使用 Microsoft Direct3D 11 API。 即使您有 Microsoft Direct3D 9 層級或 Microsoft Direct3D 10 層級的硬體，您也可以使用 Direct3D 11 API 並將目標設為 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x 或功能層級 10 \_ x 裝置。 如需有關如何使用 DirectX 開發3D 圖形的詳細資訊，請參閱 [使用 Directx 建立3d 圖形](/previous-versions/windows/apps/hh465137(v=win.10)
)。

若是2D 圖形和文字，請使用 Direct2D 和 [DirectWrite](./directwrite/direct-write-portal.md) ，而不是 Windows 圖形裝置介面 (GDI) 。

若要撰寫 Direct3D 11 或 Direct2D 填入的點陣圖，請使用 [DirectComposition](./directcomp/directcomposition-portal.md)。

若要瞭解如何建立使用 DirectX 的 Windows Store 應用程式，請參閱 [使用 Directx 建立您的第一個 Windows store 應用程式](/previous-versions/windows/apps/br229580(v=win.10)
)。 您可以使用 [**Windows. UI：： Xaml：： Controls：： SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) 類別來建立具有 Xaml UI 覆迭的高效能 DirectX 應用程式。 如需在 Windows 應用程式中結合 XAML 和 DirectX 的詳細資訊，請參閱 [DirectX 和 XAML interop](/previous-versions/windows/apps/hh825871(v=win.10))。

若要瞭解如何建立 Windows 8 的顯示驅動程式，請參閱 [Windows 顯示驅動程式模型的藍圖 (WDDM) ](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo)。

如果您需要先前 DirectX 版本的檔，請參閱 [傳統 Directx 圖形](/windows/desktop/classic-directx-graphics)。


 

 
