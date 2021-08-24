---
description: 材質 fill 函式所使用的 LPD3DXFILL2D 函數類型。
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d1407d5b6ebad18f748d5e4ba78953ad6ca543aa6df7b798aa242658a0512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846486"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

紋理填滿函數使用的函式類型。

## <a name="syntax"></a>語法


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
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

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
