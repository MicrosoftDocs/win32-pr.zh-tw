---
description: 描述色彩值。
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: 'D3DCOLORVALUE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322740"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>D3DCOLORVALUE 結構 (D3D9Types .h) 

描述色彩值。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>成員

<dl> <dt>

**r**
</dt> <dd>

類型： **float**

</dd> <dd>

指定色彩之紅色元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全沒有紅色的元件，而值1.0 則表示完全有紅色。

</dd> <dt>

**G**
</dt> <dd>

類型： **float**

</dd> <dd>

指定色彩之綠色元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全沒有綠色的元件，而值1.0 表示綠色已完全存在。

</dd> <dt>

**b**
</dt> <dd>

類型： **float**

</dd> <dd>

指定色彩之藍色元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全沒有藍色的元件，而值1.0 則表示藍色已完全存在。

</dd> <dt>

**的**
</dt> <dd>

類型： **float**

</dd> <dd>

指定色彩之 Alpha 元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全透明，而值1.0 則表示完全不透明。

</dd> </dl>

## <a name="remarks"></a>備註

您可以將此結構的成員設定為0到1範圍以外的值，以實行一些不尋常的效果。 大於1的值會產生傾向于將場景沖蝕的強大燈。 負數值會產生深亮燈，以實際從場景中移除光線。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




