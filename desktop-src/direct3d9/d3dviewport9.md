---
description: 定義3D 磁片區專案的呈現目標表面的視窗維度。
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: 'D3DVIEWPORT9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975690"
---
# <a name="d3dviewport9-structure"></a>D3DVIEWPORT9 結構

定義3D 磁片區專案的呈現目標表面的視窗維度。

## <a name="syntax"></a>語法


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a>成員

<dl> <dt>

**X**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

轉譯目標介面上，視口左上角的圖元座標。 除非您想要轉譯為介面的子集，否則這個成員可以設定為0。

</dd> <dt>

**Y**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

轉譯目標介面上，視口左上角的圖元座標。 除非您想要轉譯為介面的子集，否則這個成員可以設定為0。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

剪輯音量的寬度維度（以圖元為單位）。 除非您只轉譯為介面的子集，否則這個成員應設定為呈現目標介面的寬度維度。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

剪輯音量的高度維度（以圖元為單位）。 除非您只轉譯為介面的子集，否則這個成員應設定為轉譯目標介面的高度維度。

</dd> <dt>

**MinZ**
</dt> <dd>

類型： **float**

</dd> <dd>

搭配 MaxZ，描述要轉譯場景的深度值範圍的值，也就是剪輯音量的最小值和最大值。 大部分的應用程式會將此值設定為0.0。 套用投射矩陣之後，會執行裁剪。

</dd> <dt>

**MaxZ**
</dt> <dd>

類型： **float**

</dd> <dd>

搭配 MinZ，描述要轉譯場景的深度值範圍的值，也就是剪輯音量的最小值和最大值。 大部分的應用程式會將此值設定為1.0。 套用投射矩陣之後，會執行裁剪。

</dd> </dl>

## <a name="remarks"></a>備註

X、Y、寬度和高度成員描述轉譯目標介面上的視口位置和維度。 通常，應用程式會轉譯成整個目標介面;在 640 x 480 介面上轉譯時，這些成員應分別為0、0、640和480。 MinZ 和 MaxZ 通常會設定為0.0 和1.0，但是可以設定為其他值，以達成特定效果。 例如，您可以將它們設定為0.0，強制系統將物件轉譯為場景的前景，或同時設定為1.0 以強制物件進入背景。

當裝置的視口參數變更 (因為) 呼叫 [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) 方法時，驅動程式會建立新的轉換矩陣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
