---
description: DirectXMath 程式庫是以「運算元學 c + + SIMD 程式庫2.x 版」為基礎。 在此，我們將說明 DirectXMath 與未通過的數學有何不同，以及 DirectXMath 版本有何不同。
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: '新功能 (DirectXMath) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974576"
---
# <a name="whats-new-directxmath"></a>新功能 (DirectXMath) 

DirectXMath 程式庫是以「操作 [數學 c + + SIMD 程式庫」2.04 版](https://walbourn.github.io/)為基礎。 在此，我們將說明 DirectXMath 與未通過的數學有何不同，以及 DirectXMath 版本有何不同。

-   [Rlease 歷程記錄](#release-history)
-   [DirectXMath 與未通過數學的差異](#directxmath-differences-from-xna-math)
-   [相關主題](#related-topics)

## <a name="release-history"></a>版本歷程記錄

<table>
 <tr>
  <td>Windows 10 5 月2020更新 SDK</td><td>DirectXMath 3.14</td>
 </tr>
 <tr>
  <td>Windows 10 2018 年10月更新 SDK</td><td>DirectXMath 3.13</td>
 </tr>
 <tr>
  <td>Windows 10 2018 年4月更新 SDK<br />Windows 10 Fall Creators Update SDK</td><td>DirectXMath 3.11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update SDK</td><td>DirectXMath 3.10</td>
 </tr>
 <tr>
  <td>Windows 10 周年 SDK</td><td>DirectXMath 3.09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (2015 年11月) </td><td>DirectXMath 3.08</td>
 </tr>
 <tr>
  <td>適用于 Windows 8.1 (2015 春季的 Windows SDK) </td><td>DirectXMath 3.07</td>
 </tr>
 <tr>
  <td>Windows 8.1 的 Windows SDK</td><td>DirectXMath 3.06</td>
 </tr>
 <tr>
  <td>Windows 8 的 Windows SDK</td><td>DirectXMath 3.03</td>
 </tr>
</table>

如需詳細資訊，請參閱 [DirectXMath 版本](https://github.com/Microsoft/DirectXMath/releases) 。

## <a name="directxmath-differences-from-xna-math"></a>DirectXMath 與未通過數學的差異

以下是 DirectXMath 程式庫主要與「運算元學」程式庫有何不同：

-   DirectXMath 僅限 c + + (命名空間、多載、新範本等) 。
-   需要 c + + 11 標準程式庫支援 (也就是在) 上的 stdint.h。
-   Windows RT 平臺的 ARM 霓虹燈內建支援。
-   新的色彩功能 (色彩空間轉換、.NET 色彩常數) 。
-   界限磁片區類型 (先前在 DirectX SDK 衝突範例) 的 XNACollision 標頭中的版本。
-   沒有 Xbox 360 版本可供使用。 Xbox 360 XDK 會繼續寄送 XNAMath v2. x;移除 Xbox 360 特定的資料類型和函數變異。
-   修改 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) ，以改善 SSE 和 ARM 霓虹燈內建函式的優化。
-   [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)類型完全不透明。 若要存取 **XMMATRIX** 的個別元素，請使用其他類型，例如 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計指南](ovw-xnamath-progguide.md)
</dt> <dt>

[DirectXMath 版本](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
