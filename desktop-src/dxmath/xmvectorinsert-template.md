---
description: 將向量旋轉指定的32位元件數目，並將該結果的選取元素插入另一個向量。
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: 'XMVectorInsert template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90eb7348639e6993cb69ef9e82ab78ed989999ea8423f1f6ff8bd9deb7c70d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739749"
---
# <a name="xmvectorinsert-template"></a>XMVectorInsert 範本

將向量旋轉指定的32位元件數目，並將該結果的選取元素插入另一個向量。

## <a name="syntax"></a>語法

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*VD*
</dt> <dd>

\[\]要插入的向量。

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*與*
</dt> <dd>

\[\]以向量向左旋轉。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳迴旋轉和插入所產生的 [**XMVECTOR**](xmvector-data-type.md) 。

## <a name="remarks"></a>備註

此函數是 [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert)的範本版本，其中 *Select \** 引數是範本值。

為了達到最佳效能， `XMVectorInsert` 應該將的結果指派回 *VD*。

> [!Note]  
> `XMVectorInsert`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
