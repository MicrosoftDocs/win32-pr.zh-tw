---
description: Permutes 兩個向量的元件來建立新的向量。
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: 'XMVectorPermute template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990831"
---
# <a name="xmvectorpermute-template"></a>XMVectorPermute 範本

Permutes 兩個向量的元件來建立新的向量。

## <a name="syntax"></a>語法

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[\]第一個向量。

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*2*
</dt> <dd>

\[\]第二個向量。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回合並來源向量所產生的排列向量。

## <a name="remarks"></a>備註

如果所有4個索引只參考單一向量 (也就是它們全都在0-3 範圍內，或在 4-7) 的所有範圍內，請改用 [**XMVectorSwizzle**](xmvectorswizzle-template.md) 來提升效能。

請注意，程式庫會在某些平臺上使用範本特製化，以改善效能。 並非每個可能的鏡像案例都是針對這些特殊情況所執行，因此最好是 permutes，其中產生之向量的 X 元素來自 V1 參數，而不是 V2 參數。 例如，偏好使用 `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);` 。

此函式是 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的範本版本，其中 *置換 \** 引數是範本值。

提供 [了 \_ XM \_ 置換](ovw-xnamath-reference-constants.md)常數作為 *PermuteX*、*PermuteY*、*PermuteZ* 和 *PermuteW* 的輸入值使用。

> [!Note]  
> `XMVectorPermute`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。

 

**命名空間**：使用 DirectX

### <a name="platform-requirements"></a>平台需求

Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。 Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DirectXMath。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectXMath 程式庫範本函數](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
