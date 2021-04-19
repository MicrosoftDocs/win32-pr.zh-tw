---
description: 使用特定的材質篩選器產生 mipmap 鏈。
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: 'D3DX10FilterTexture 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990012"
---
# <a name="d3dx10filtertexture-function"></a>D3DX10FilterTexture 函式

使用特定的材質篩選器產生 mipmap 鏈。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTexture* 
</dt> <dd>

類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

要篩選的材質物件。 請參閱 [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。

</dd> <dt>

*SrcLevel* 
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

Mipmap 層級的資料會用來產生 mipmap 鏈的其餘部分。

</dd> <dt>

*MipFilter* 
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

旗標控制每個 miplevel 的篩選方式 (或 D3DX10 \_ D3DX10 篩選方塊) 的預設值 \_ \_ 。 請參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md)標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 10 中的材質函數](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
