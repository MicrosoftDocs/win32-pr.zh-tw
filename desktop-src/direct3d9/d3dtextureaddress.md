---
description: 定義常數，以描述支援的材質定址模式。
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: 'D3DTEXTUREADDRESS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035338"
---
# <a name="d3dtextureaddress-enumeration"></a>D3DTEXTUREADDRESS 列舉

定義常數，以描述支援的材質定址模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ WRAP**
</dt> <dd>

並排顯示每個整數連接點的材質。 例如，如果您的值介於0和3之間，則紋理會重複三次;不執行鏡像。

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS \_ 鏡像**
</dt> <dd>

類似于 D3DTADDRESS \_ WRAP，不同之處在于材質會在每個整數連接點翻轉。 例如，如果您的值介於0和1之間，則會以正常方式定址紋理;在1和2之間，紋理會 (鏡像) 翻轉;在2和3之間，紋理會再次正常;依此類推。

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ 夾具**
</dt> <dd>

在0.0 範圍之外的材質座標 \[ ，1.0 \] 會分別設定為0.0 或1.0 的材質色彩。

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS \_ 框線**
</dt> <dd>

在0.0 範圍之外的材質座標 \[ ，1.0 \] 會設定為框線色彩。

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**
</dt> <dd>

類似于 D3DTADDRESS \_ 鏡像和 D3DTADDRESS \_ 夾具。 採用紋理座標的絕對值 (因此，鏡像大約為 0) ，然後個至最大值。 最常見的用法是針對磁片區紋理，其中不需要完整 D3DTADDRESS \_ MIRRORONCE 材質定址模式的支援，但資料在一個座標軸周圍是對稱的。

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
