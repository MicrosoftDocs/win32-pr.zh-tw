---
description: 描述 DirectXMath 程式庫類型和結構。
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: DirectXMath 程式庫結構
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ac040ee932e9da84c186124514d9f763e20e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318775"
---
# <a name="directxmath-library-structures"></a>DirectXMath 程式庫結構

描述 DirectXMath 程式庫類型和結構。

DirectXMath 程式庫提供許多結構和定義型別來封裝資料，以支援容易使用、優化和可攜性。 下列清單包含目前 DirectXMath 程式庫的一部分結構。 它們可透過 DirectXMath 取得。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | 2D 向量，其中每個元件都是帶正負號的整數，8位 (1 位元組) 長度。 |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | 每個元件都是帶正負號的整數、8位 (1 位元組) 長度的4D 向量。  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | 2D 向量，用來將已簽署的正規化值儲存為帶正負號的8位 (1 位元組) 整數。 |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | 將已簽署的正規化值儲存為帶正負號的8位 (1 個位元組) 整數的3D 向量。  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | 32位 Alpha 紅色綠色藍色 (ARGB) 色向量，其中每個顏色通道都指定為不帶正負號的8位整數。 |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | 具有 x、y 和 z 元件的4D 向量，表示為10位帶正負號的整數值，而 w 元件則為2位帶正負號的整數值。  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | 用來將已簽署、正規化的值儲存為10位帶正負號之 x、y 和 z 元件，以及2位帶正負號之 w 元件的4D 向量。  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | 由兩個單精確度浮點值所組成的2D 向量。 |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | 描述在16位元組的界限上對齊的 [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) 結構。 |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | 描述包含三個單精確度浮點值的3D 向量。 |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | 描述在16位元組的界限上對齊的 [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) 結構。 |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | 描述3D 向量，其 X 和 Y 元件儲存為11位浮點數，而 Z 元件儲存為10位浮點值。  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | 描述具有9位尾數之三個浮點元件的3D 向量，每個都共用相同的5位指數。  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | 3x3 浮點數矩陣。 |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | 包含32位浮點元件的3x4 圓資料行主要矩陣。 |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | 3x4 圓的資料行主要矩陣，其中包含在16位元組的界限上對齊的32位浮點元件。 |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | 描述由四個單精確度浮點值所組成的4D 向量。  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | 描述在16位元組的界限上對齊的 [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) 結構。 |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | 4x3 浮點數矩陣。 |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | 描述在16位元組的界限上對齊的 [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) 結構。 |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | 4x4 浮點數矩陣。 |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | 描述在16位元組的界限上對齊的 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) 結構。 |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | 2D 向量，由兩個半精確度 (16bit) 浮點值所組成。  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | 描述由四個半精確度 (16 位) 浮點數所組成的4D 向量。  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | 2D 向量，其中每個元件都是帶正負號的整數。 |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | 每個元件都是帶正負號整數的3D 向量。 |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | 每個元件都是帶正負號整數的4D 向量。 |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | 描述對應至四個硬體向量暫存器之16位元組界限上的4x4 矩陣。 |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | 描述由16位帶正負號和正規化的整陣列件所組成的2D 向量。  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | 由16位帶正負號的整陣列件所組成的4D 向量。  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | 將已簽署的正規化值儲存為帶正負號16位整數的2D 向量 (類型 `int16_t`) 。  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | 用來將已簽署的正規化值儲存為帶正負號16位整數的4D 向量， (類型 `int16_t`) 。  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | 具有 x、y 和 z 元件的4D 向量，表示為5位不帶正負號的整數值，以及 w 元件的1位整數值。  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | 具有 x 和 z 元件的3D 向量，表示為5位不帶正負號的整數值，而 y 元件為6位不帶正負號的整數值。 |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | 描述2D 向量，其中每個元件都是不帶正負號的整數，8位 (1 位元組) 長度。 |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | 描述每個元件都是不帶正負號的整數、8位 (1 位元組) 長度的4D 向量。  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | 2D 向量，用來將未簽署的正規化值儲存為帶正負號的8位 (1 位元組) 整數。 |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | 將未簽署的正規化值儲存為帶正負號的8位 (1 個位元組) 整數的3D 向量。  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | 具有 x、y 和 z 元件的4D 向量，表示為10位不帶正負號的整數值，而 w 元件為2位不帶正負號的整數值。  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | 用來將未簽署、正規化的整數值儲存為10位不帶正負號 x、y 和 z 元件，以及2位不帶正負號 w 元件的4D 向量。  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | 2D 向量，其中每個元件都是不帶正負號的整數。 |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | 三維向量，其中每個元件都是不帶正負號的整數。 |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | 4D 向量，其中每個元件都是不帶正負號的整數。 |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | 具有四個不帶正負號4位整陣列件的4D 向量。  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | 描述包含16位不帶正負號整陣列件的2D 向量。  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | 由16位不帶正負號整陣列件所組成的4D 向量。  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | 將未簽署的正規化值儲存為不帶正負號16位整數的2D 向量， (類型 `uint16_t`) 。  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | 用來將未簽署的正規化值儲存為帶正負號之16位整數的4D 向量 (類型 `uint16_t`) 。  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | 具有 x、y 和 z 元件的4D 向量，表示為10位帶正負號的整數值，而 w 元件為2位不帶正負號的整數值。  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | 用來將已簽署的正規化值（以10位帶正負號的 x、y 和 z 元件，以及不帶正負號的正規化值）儲存為2位不帶正負號 w 元件的4D 向量。  |

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計參考](ovw-xnamath-reference.md)
</dt> </dl>
