---
description: 將向量向右旋轉指定的32位元素數目。
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: 'XMVectorRotateRight template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47017982af6bb61212129665010d403bd9db898c65056110c4d2f40a5f8a9362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984488"
---
# <a name="xmvectorrotateright-template"></a>XMVectorRotateRight 範本

將向量向右旋轉指定的32位元素數目。

## <a name="syntax"></a>語法

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[\]以向量向右旋轉。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳迴旋轉的 [**XMVECTOR**](xmvector-data-type.md)。

## <a name="remarks"></a>備註

此函式是範本版本的 [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) ，其中 *Elements* 引數是範本值。

> [!Note]  
> `XMVectorRotateRight`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。

 

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
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
