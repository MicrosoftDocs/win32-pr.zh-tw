---
description: 定義材質座標轉換值。
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: 'D3DTEXTURETRANSFORMFLAGS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196199"
---
# <a name="d3dtexturetransformflags-enumeration"></a>D3DTEXTURETRANSFORMFLAGS 列舉

定義材質座標轉換值。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ DISABLE**
</dt> <dd>

材質座標會直接傳遞至轉譯器。

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

轉譯器應該預期是1D 材質座標。 Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

轉譯器應預期2D 材質座標。 Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

轉譯器應預期3D 紋理座標。 Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

轉譯器應預期為4D 材質座標。 Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ 投射**
</dt> <dd>

固定函式圖元管線會採用此旗標，以及將 ps 1 1 版本中的可程式化圖元管線視為 \_ \_ ps \_ 1 \_ 3。 針對材質階段啟用紋理投影時，全部四個浮點值都必須寫入對應的材質暫存器。 每個材質座標都會先除以最後一個元素，然後再傳遞給轉譯器。 例如，如果使用 D3DTTFF COUNT3 旗標來指定此旗標 \_ ，則第一個和第二個材質座標會先除以第三個座標，再傳遞給轉譯器。

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用 4 x 4 矩陣來轉換材質座標，然後將結果傳遞給轉譯器。 紋理座標轉換的設定方式是呼叫 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api)，並傳入 D3DTSS \_ TEXTURETRANSFORMFLAGS 材質階段狀態和 **D3DTEXTURETRANSFORMFLAGS** 中的其中一個值。 如需紋理轉換的詳細資訊，請參閱 [ (Direct3D 9) 的材質座標轉換 ](texture-coordinate-transformations.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
