---
description: Direct3D 是一個低層級的 API，用來繪製具有轉譯管線的基本專案，或使用計算著色器執行平行作業。
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: 開始使用 Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea01f24659bfbb5eb0667a0ae1cbfa3529a206b7b7ce7e3d3a4388e71fabd571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092548"
---
# <a name="getting-started-with-direct3d"></a>開始使用 Direct3D

Direct3D 是一個低層級的 API，用來繪製具有轉譯管線的基本專案，或是用來執行具有計算著色器的平行作業。

## <a name="what-is-direct3d"></a>什麼是 Direct3D？

Direct3D 是低層級的 API，可讓您用來繪製每個框架的三角形、線條或點，或在 GPU 上啟動高度平行的作業。

Direct3D

-   隱藏一致抽象概念背後的不同 GPU 執行。 但是您仍然需要知道如何繪製3D 圖形。
-   是設計來驅動個別的圖形專用處理器。 較新的 Gpu 具有數百個或數千個平行處理器。
-   強調平行處理。 您可以設定一連串的轉譯或計算狀態，然後開始操作。 您不會等待作業立即提出意見反應。 您不會混合 CPU 和 GPU 作業。

## <a name="which-direct3d-apis-can-you-use"></a>您可以使用哪些 Direct3D Api？

您所選擇的 Direct3D Api 取決於您要撰寫的應用程式樣式。

-   如果您想要撰寫 UWP 應用程式，請使用 Direct3D 11、DXGI 和 HLSL Api 的子集。 如需這些 Api 的清單，請參閱 [適用于 UWP 應用程式的 Win32 和 COM api](/uwp/win32-and-com/win32-and-com-for-uwp-apps)。 若要瞭解如何撰寫 Direct3D 11 Windows Store 應用程式，請參閱[使用 DirectX 建立3d 圖形](/previous-versions/windows/apps/hh465137(v=win.10))。
-   如果您撰寫桌面應用程式，您可以使用一組完整的 Direct3D 11、DXGI 和 HLSL Api。
-   從 Windows 8 開始，我們不會再主動支援適用于傳統型應用程式的「使用」架構。 但 Windows Store 應用程式、UWP 應用程式和桌面應用程式可以使用完整的[XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal)和[DirectXMath](/windows/desktop/dxmath/directxmath-portal) api 集合。 桌面應用程式可以使用一組完整的[XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) api，而 Windows Store 應用程式和 UWP 應用程式可以使用大部分的 XInput api;如需詳細資訊，請參閱[XInput 版本](/windows/desktop/xinput/xinput-versions)。

## <a name="which-direct3d-version"></a>哪個 Direct3D 版本？

您所選擇的 Direct3D API 版本取決於您要作為目標的作業系統和硬體層級。

-   如果您想要以 Windows 8 和更新版本為目標，請使用 Direct3D 11 api。
-   使用 Direct3D 9 api 搭配 Windows XP 及更新版本。 所有硬體都支援 Direct3D 9 Api （甚至是較新的 Direct3D 11 層級硬體）。
-   使用 Direct3D 10 api 搭配 Windows Vista 和更新版本。 只有 Direct3D 10 層級和更新版本的硬體支援 Direct3D 10 Api。
-   使用 direct3d 10.1 和 direct3d 11 api 搭配 Windows 7 和更新版本。 您也可以下載[KB 971644](https://support.microsoft.com/kb/971644)，將 direct3d 10.1 和 direct3d 11 api 搭配 Windows Vista Service Pack 2 (SP2) 。

## <a name="direct3d-rendering-pipeline"></a>Direct3D 轉譯管線

在 Direct3D 轉譯 [管線](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)中，資料會從數個來源（例如，tributaries）進行流動。

-   流程的某些部分是可程式化的。
-   有些部分具有旋鈕和撥號。
-   資料來源是封包 (頂點的序列串流) 或可編制索引的陣列 (著色器資源) 。
-   頂點和著色器資源會流入可增強的基本專案。
-   基本和著色器資源會流入圖元作業。

## <a name="direct3d-compute-shader"></a>Direct3D 計算著色器

使用 Direct3D [計算著色器](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)，所有 GPU 的處理器都會平行執行。 因此，計算著色器的行為就像是 pond。
