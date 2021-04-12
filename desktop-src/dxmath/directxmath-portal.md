---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321776"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>目的

DirectXMath API 提供 SIMD 的 c + + 類型和函式，適用于 DirectX 應用程式常見的一般線性代數和圖形數學運算。 此程式庫會透過 Visual C++ 編譯器中的 SSE、AVX 和 ARM-霓虹燈內建支援，提供 Windows 32 位的優化版本 (x86) 、Windows 64 位 (x64) ，以及 ARM/ARM64 上的 Windows。

針對剛 DirectXMath 的開發人員，您可能想要考慮在 directx [11](https://go.microsoft.com/fwlink/?LinkId=248929)DirectX12 的 *directx 工具套件* 中使用 SimpleMath 包裝函式  /  [](https://go.microsoft.com/fwlink/?LinkID=615561)作為起點。

## <a name="in-this-section"></a>本節內容



| 主題                                                                     | 描述                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [DirectXMath 程式設計指南](ovw-xnamath-progguide.md)<br/>     | DirectXMath 提供針對 Windows 優化的數學解決方案。<br/>           |
| [DirectXMath 程式設計參考](ovw-xnamath-reference.md)<br/> | 本章節包含 DirectXMath 程式庫的參考資料。<br/> |



 

## <a name="developer-audience"></a>開發人員對象

DirectXMath 程式庫是專為 c + + 開發人員所設計，適用于在 Windows Store 應用程式、Xbox 遊戲和 Windows 的傳統桌面應用程式中使用遊戲和 DirectX 圖形的程式。

## <a name="obtaining-directxmath"></a>取得 DirectXMath
 
DirectXMath 標頭隨附于 Visual Studio 2012 （含）以後版本隨附的 Windows SDK，而作為所有內嵌標頭時，不會連結任何 DLL 或靜態程式庫。 它也可做為 [NuGet](https://www.nuget.org/packages/directxmath/)上的套件。

DirectXMath 是在[GitHub](https://github.com/Microsoft/DirectXMath)上裝載之[MIT 授權](https://opensource.org/licenses/MIT)下的開放原始碼。




