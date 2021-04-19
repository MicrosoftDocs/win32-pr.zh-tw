---
description: 定義支援的 blend 作業。 請參閱備註中的詞彙定義。
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: 'D3DBLENDOP 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988174"
---
# <a name="d3dblendop-enumeration"></a>D3DBLENDOP 列舉

定義支援的 blend 作業。 請參閱備註中的詞彙定義。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ 新增**
</dt> <dd>

結果會是新增至來源的目的地。 結果 = 來源 + 目的地

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP \_ 減**
</dt> <dd>

結果是從目的地減去至來源的目的地。 結果 = 來源-目的地

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**
</dt> <dd>

結果會從目的地減去來源。 結果 = 目的地-來源

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ 分鐘**
</dt> <dd>

結果是來源和目的地的最小值。 結果 = 最小 (來源，目的地) 

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ MAX**
</dt> <dd>

結果是來源和目的地的最大值。 結果 = 最大 (來源，目的地) 

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

來源、目的地和結果定義如下：



| 詞彙        | 類型   | 描述                                                            |
|-------------|--------|------------------------------------------------------------------------|
| 來源      | 輸入  | 運算之前的來源圖元色彩。                        |
| Destination | 輸入  | 作業之前，目的緩衝區中圖元的色彩。     |
| 結果      | 輸出 | 傳回的值是作業所產生的混合色彩。 |



 

這個列舉型別會定義下列轉譯狀態所使用的值：

-   D3DRS \_ BLENDOP
-   D3DRS \_ BLENDOPALPHA

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
