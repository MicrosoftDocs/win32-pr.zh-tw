---
description: 定義旗標，用來控制執行 multimatrix 頂點混合時，系統所套用的數位或矩陣。
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: 'D3DVERTEXBLENDFLAGS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecc7f99e26088ff03b626604279bffe5c64ddb82b95a6f6219b637b3fce5a59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527302"
---
# <a name="d3dvertexblendflags-enumeration"></a>D3DVERTEXBLENDFLAGS 列舉

定義旗標，用來控制執行 multimatrix 頂點混合時，系統所套用的數位或矩陣。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ DISABLE**
</dt> <dd>

停用頂點混合;只套用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定的世界矩陣，其中轉換狀態的索引值為0。

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

啟用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定之兩個矩陣之間的頂點混合，其中轉換狀態的索引值為0和1。

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

啟用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定之三個矩陣之間的頂點混合，其中轉換狀態的索引值為0、1和2。

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

啟用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定之四個矩陣之間的頂點混合，其中轉換狀態的索引值為0、1、2和3。

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF \_ 補間**
</dt> <dd>

您可以使用指派給 D3DRS TWEENFACTOR 的值來完成頂點混色 \_ 。

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

使用權數為1.0 的單一矩陣。

</dd> </dl>

## <a name="remarks"></a>備註

此類型的成員會搭配 D3DRS VERTEXBLEND 轉譯 \_ 狀態使用。

幾何混合 (multimatrix 頂點混色) 需要您的應用程式使用已針對每個頂點混合 (Beta) 權數的頂點格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ 世界**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
