---
description: D3DX 是一種專為在 Direct3D 之上提供其他圖形功能而設計的工具程式庫。 D3DX 是以動態連結程式庫的形式提供， (DLL) 。
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: 'D3DX (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556d1f7dfe7f8d841220af4f5dbe650bd74e4c8dff86812650545a07129af644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986908"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9) 

> [!NOTE]
> D3DX 程式庫已被取代。 如果無法選擇升級至較新版本的 Direct3D 和相關聯的公用程式程式碼，您可以使用[DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件，而不是依賴舊版 DirectX SDK 或 DirectSetup。

D3DX 是一種專為在 Direct3D 之上提供其他圖形功能而設計的工具程式庫。 D3DX 是以動態連結程式庫的形式提供， (DLL) 。

這一版的 DirectX SDK 只提供一個版本的 D3DX。 零售 D3DX DLL 包含在 SDK 所提供的可轉散發套件中，並會在 **使用 DirectSetup 安裝 DirectX** 的過程中自動安裝。 此版本中包含的 D3DX 程式庫相依于此 SDK 隨附的 Direct3D 執行時間。 在此版本中連結至 D3DX 版本的應用程式，也必須從這個 SDK 轉散發執行時間。

多個版本的 D3DX 可同時在單一系統上獨立放置。 藉由將應用程式以靜態方式連結至 D3dx9，應用程式會在執行時間動態連結至對應的零售 D3DX DLL。 此 DLL 對應于 D3DX 標頭，此應用程式會針對在 \_ \_) D3dx9core 中以 D3DX SDK 版本常數命名的 (進行編譯。 當新版本的 D3DX 在未來的 DirectX SDK 版本中寄出時，連結至舊版 D3DX 程式庫的應用程式仍不會受到影響。

D3DX 程式庫會解決這些一般功能區域：

-   [D3DX 中的線條繪圖支援 (Direct3D 9) ](line-drawing-support-in-d3dx.md)
-   [D3DX 中的網格支援 (Direct3D 9) ](mesh-support-in-d3dx.md)
-   [D3DX (Direct3D 9) 中的數學函數支援 ](math-function-support-in-d3dx.md)
-   [D3DX 中的材質支援 (Direct3D 9) ](texture-support-in-d3dx.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> </dl>

 

 



