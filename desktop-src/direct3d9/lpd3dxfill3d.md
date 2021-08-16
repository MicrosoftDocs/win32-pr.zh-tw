---
description: 材質 fill 函式所使用的 LPD3DXFILL3D 函數類型。
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399c711b550124cf93889640277d86b8669e20b1dfc33b2d3865f73b29e85e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799430"
---
# <a name="lpd3dxfill3d"></a>LPD3DXFILL3D

紋理填滿函數使用的函式類型。

## <a name="syntax"></a>語法


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>參數

不悅-函數用來傳回結果的向量指標。 X、Y、Z 和 W 會分別對應至 R、G、B 和 A。

pTexCoord-向量的指標，其中包含目前正在評估之材質的座標。 材質和音量紋理的材質座標元件範圍從0到1。 Cube 紋理的材質座標元件範圍從-1 到1。

pTexelSize-包含目前材質之維度的向量指標。

.Pdata-使用者資料的指標。

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md)呼叫慣例。 否則，可能會發生堆疊溢位。



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3dx9tex。h |
| 匯入程式庫           | d3dx9 .lib  |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[回呼函式](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL2D](lpd3dxfill2d.md)
</dt> </dl>

 

 
