---
description: 針對材質物件中的每個材質設定一般向量。 如果) 計算以圖元為基礎的預先計算 radiance 傳輸 (PRT) ，則會使用這個方法來儲存網格 (中的頂點一般向量或插入頂點法線。
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine：： SetPerTexelNormal 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386477"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>ID3DXPRTEngine：： SetPerTexelNormal 方法

針對材質物件中的每個材質設定一般向量。 如果) 計算以圖元為基礎的預先計算 radiance 傳輸 (PRT) ，則會使用這個方法來儲存網格 (中的頂點一般向量或插入頂點法線。

## <a name="syntax"></a>語法


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNormalTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

指向 [**IDirect3DTexture9**](/windows/desktop/api) 材質物件的指標，此物件可作為物件空間一般地圖以用來儲存一般向量。 材質必須具有與 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 相同的維度，而且必須能夠儲存已簽署的材質格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
