---
description: Swizzles 向量。
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: 'XMVectorSwizzle template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800d976d63480f88defea7f1db07651563df44e8985ae5925810617b44302e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984478"
---
# <a name="xmvectorswizzle-template"></a>XMVectorSwizzle 範本

Swizzles 向量。

## <a name="syntax"></a>語法

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[在 \] 向量中 swizzle。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 swizzled [**XMVECTOR**](xmvector-data-type.md)。

## <a name="remarks"></a>備註

此函式是 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle)的範本版本，其中 *Swizzle \** 引數是範本值。

`XM_SWIZZLE_X`、 `XM_SWIZZLE_Y` 、 `XM_SWIZZLE_Z` 和 `XM_SWIZZLE_W` 都是分別評估為0、1、2和3的常數，以搭配使用 `XMVectorSwizzle` 。 這與 `XM_PERMUTE_0X` 、 `XM_PERMUTE_0Y` 、和相同 `XM_PERMUTE_0Z` `XM_PERMUTE_0W` 。

> [!Note]  
> `XMVectorSwizzle`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。

 

**命名空間**：使用 DirectX

### <a name="platform-requirements"></a>平台需求

Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。 支援 Win32 傳統型應用程式、Windows 儲存應用程式，以及 Windows Phone 8 個應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DirectXMath。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectXMath 程式庫範本函數](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> </dl>

 

 
