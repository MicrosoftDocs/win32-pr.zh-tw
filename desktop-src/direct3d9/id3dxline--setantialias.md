---
description: 切換線條消除鋸齒。
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine：： SetAntialias 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1214b4c045494d3f7ec7f72e94570231b2b84c430759a619491cf8f34869c942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120882"
---
# <a name="id3dxlinesetantialias-method"></a>ID3DXLine：： SetAntialias 方法

切換線條消除鋸齒。

## <a name="syntax"></a>語法


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bAntiAlias* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

切換消除鋸齒功能。 **TRUE** 會開啟消除鋸齒，而 **FALSE** 則會關閉消除鋸齒功能。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::GetAntialias**](id3dxline--getantialias.md)
</dt> </dl>

 

 
