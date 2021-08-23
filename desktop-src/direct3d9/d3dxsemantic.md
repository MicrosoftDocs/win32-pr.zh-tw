---
description: 將參數對應至頂點或圖元著色器暫存器的語法。 它們也可以是附加至非註冊參數的選擇性描述性字串。
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: 'D3DXSEMANTIC 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2534df72c246fdec361597a8e156f7f19b341ae35fcc04b3bdc6eb71c2903fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631018"
---
# <a name="d3dxsemantic-structure"></a>D3DXSEMANTIC 結構

將參數對應至頂點或圖元著色器暫存器的語法。 它們也可以是附加至非註冊參數的選擇性描述性字串。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>成員

<dl> <dt>

**使用量**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

識別如何使用資源的選項。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。

</dd> <dt>

**UsageIndex**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

修改如何解讀使用方式的選項。 使用方式和使用方式索引組成頂點宣告。 請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。

</dd> </dl>

## <a name="remarks"></a>備註

頂點和圖元著色器、輸入和輸出暫存器需要有語義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
