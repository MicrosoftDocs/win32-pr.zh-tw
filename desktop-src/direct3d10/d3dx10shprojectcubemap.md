---
description: 將 cube 地圖中表示的函式投射到球面諧波。
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: 'D3DX10SHProjectCubeMap 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fa30724bed56e86d16626133ab32e3494d3c71d6ffa839be1520518c97a77fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990458"
---
# <a name="d3dx10shprojectcubemap-function"></a>D3DX10SHProjectCubeMap 函式

將 cube 地圖中表示的函式投射到球面諧波。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*順序* 
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序會產生 Order ^ 2 coefs，度數為 Order-1。

</dd> <dt>

*pCubeMap* 
</dt> <dd>

類型： **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

即將投射到球形諧波的立方體貼圖。 請參閱 [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)。

</dd> <dt>

*pROut* 
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

紅色的輸出 SH 向量。

</dd> <dt>

*pGOut* 
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

綠色的輸出 SH 向量。

</dd> <dt>

*pBOut* 
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

藍色的輸出 SH 向量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
