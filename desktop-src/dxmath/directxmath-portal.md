---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a041696daf5d5cad8467d01f8ef7912d177ba63a7193945b4cb52a430f4afc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118501765"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>目的

DirectXMath API 提供 SIMD 的 c + + 類型和函式，適用于 DirectX 應用程式常見的一般線性代數和圖形數學運算。 此程式庫針對 Windows 32 位 (x86) 、Windows 64 位 (x64) ，以及 Windows 編譯器中的 SSE、AVX 和 arm-霓虹燈內建支援，提供 arm/ARM64 的優化版本。

針對剛 DirectXMath 的開發人員，您可能想要考慮在 directx [11](https://go.microsoft.com/fwlink/?LinkId=248929)DirectX12 的 *directx 工具套件* 中使用 SimpleMath 包裝函式  /  [](https://go.microsoft.com/fwlink/?LinkID=615561)作為起點。

## <a name="in-this-section"></a>本節內容



| 主題                                                                     | 描述                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [DirectXMath 程式設計指南](ovw-xnamath-progguide.md)<br/>     | DirectXMath 提供針對 Windows 優化的數學解決方案。<br/>           |
| [DirectXMath 程式設計參考](ovw-xnamath-reference.md)<br/> | 本章節包含 DirectXMath 程式庫的參考資料。<br/> |



 

## <a name="developer-audience"></a>開發人員對象

DirectXMath 程式庫是專為 c + + 開發人員所設計，可在 Windows 店內的應用程式、Xbox 遊戲和傳統桌面應用程式中使用遊戲和 DirectX 圖形來進行 Windows。

## <a name="obtaining-directxmath"></a>取得 DirectXMath
 
DirectXMath 標頭隨附于 Visual Studio 2012 （含）以後版本隨附的 Windows SDK，而作為所有內嵌標頭時，不會連結任何 DLL 或靜態程式庫。 也可在[NuGet](https://www.nuget.org/packages/directxmath/)上以套件的形式提供。

DirectXMath 是裝載于[GitHub](https://github.com/Microsoft/DirectXMath)之[MIT 授權](https://opensource.org/licenses/MIT)下的開放原始碼。




