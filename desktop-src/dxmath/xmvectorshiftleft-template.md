---
description: 將向量向左移位指定數目的32位元素，並使用第二個向量的元素來填滿空的元素。
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: 'XMVectorShiftLeft template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982651"
---
# <a name="xmvectorshiftleft-template"></a>XMVectorShiftLeft 範本

將向量向左移位指定數目的32位元素，並使用第二個向量的元素來填滿空的元素。

## <a name="syntax"></a>語法

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[\]以向量向左移。

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*2*
</dt> <dd>

\[在中， \] 用來在左移左方元件之後，用來填入該元件的。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回移位並填滿 [**XMVECTOR**](xmvector-data-type.md)。

## <a name="remarks"></a>備註

此函式是範本版本的 [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) ，其中 *Elements* 引數是範本值。

> [!Note]  
> `XMVectorShiftLeft`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
