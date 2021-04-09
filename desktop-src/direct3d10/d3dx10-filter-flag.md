---
description: 材質篩選旗標。
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: 'D3DX10_FILTER_FLAG 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f12842cd07c55c33509ecfbb56fc804a6fc3b7c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946224"
---
# <a name="d3dx10_filter_flag-enumeration"></a>D3DX10 \_ 篩選 \_ 旗標列舉

材質篩選旗標。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10 \_ 篩選 \_ 無**
</dt> <dd>

不會進行調整或篩選。 來源影像界限外的圖元會假設為透明的黑色。

</dd> <dt>

<span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10 \_ 篩選 \_ 點**
</dt> <dd>

每個目的地圖元都是從來源影像取樣最接近的圖元來計算。

</dd> <dt>

<span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10 \_ 篩選 \_ 線性**
</dt> <dd>

每個目的地圖元都是從來源影像取樣四個最接近的圖元來計算。 當兩個軸的刻度小於2時，此篩選器的效果最佳。

</dd> <dt>

<span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10 \_ 篩選 \_ 三角形**
</dt> <dd>

來源影像中的每個圖元平均占目的地映射。 這是篩選器的最慢。

</dd> <dt>

<span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10 \_ 篩選 \_ 方塊**
</dt> <dd>

每個圖元的計算方式是將來源影像中的 2x2 (x2) box 圖元平均。 只有當目的地的維度為來源的一半時，此篩選才會運作，如同 mipmap 的情況。

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10 \_ 篩選 \_ 鏡像 \_ U**
</dt> <dd>

U 軸上材質邊緣的圖元應進行鏡像，而不會換行。

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10 \_ 篩選 \_ 鏡像 \_ V**
</dt> <dd>

在 v 軸上紋理邊緣的圖元應進行鏡像，而不會換行。

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10 \_ 篩選 \_ 鏡像 \_ W**
</dt> <dd>

在 w 軸上紋理邊緣的圖元應進行鏡像，而不會換行。

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10 \_ 篩選 \_ 鏡像**
</dt> <dd>

指定此旗標與指定 D3DX \_ 濾波器 \_ 鏡像 \_ U、D3DX \_ FILTER \_ 鏡像 \_ V 和 D3DX \_ 濾波器 \_ mirror （ \_ W 旗標）相同。

</dd> <dt>

<span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10 \_ 篩選 \_ 遞色**
</dt> <dd>

產生的影像必須使用4x4 排序的遞色量演算法進行遞色。 從某種格式轉換成另一種格式時，就會發生此問題。

</dd> <dt>

<span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10 \_ 篩選 \_ 遞色 \_ 擴散**
</dt> <dd>

從某種格式變更為另一種格式時，對影像進行擴散遞色。

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ FILTER \_ SRGB \_ IN**
</dt> <dd>

輸入資料是在標準 RGB (sRGB) 色彩空間中。 請參閱＜備註＞。

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ FILTER \_ SRGB \_ OUT**
</dt> <dd>

輸出資料是在標準 RGB (sRGB) 色彩空間中。 請參閱＜備註＞。

</dd> <dt>

<span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ 篩選 \_ SRGB**
</dt> <dd>

與 \_ \_ \_ 在 \| D3DX \_ 篩選 \_ srgb 中 \_ 指定 D3DX 篩選 srgb 的方式相同。 請參閱＜備註＞。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX10 會自動執行 gamma 更正 (將色彩資料從 RGB 空間轉換成標準的 RGB 空間，) 載入材質資料時。 當 RGB 資料從 .png 檔案載入至 sRGB 材質時，就會自動完成這項操作。 使用 SRGB 篩選旗標來指出資料是否不需要轉換成 sRGB 空間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




