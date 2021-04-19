---
description: 將向量向左旋轉指定的32位元素數目。
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: 'XMVectorRotateLeft template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000412"
---
# <a name="xmvectorrotateleft-template"></a>XMVectorRotateLeft 範本

將向量向左旋轉指定的32位元素數目。

## <a name="syntax"></a>語法

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[\]以向量向左旋轉。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳迴旋轉的 [**XMVECTOR**](xmvector-data-type.md)。

## <a name="remarks"></a>備註

此函式是範本版本的 [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) ，其中 *Elements* 引數是範本值。

> [!Note]  
> `XMVectorRotateLeft`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
