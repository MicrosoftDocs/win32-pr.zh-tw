---
description: 將每個預先計算 radiance 傳輸 (PRT) 向量乘以每個頂點 >albedo。
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine：： MultiplyAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2989ce2a662be5a1ec53c961b8fafa072862fc2b43b6003b04f6b887ef3c077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790538"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>ID3DXPRTEngine：： MultiplyAlbedo 方法

將每個預先計算 radiance 傳輸 (PRT) 向量乘以每個頂點 >albedo。

## <a name="syntax"></a>語法


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件將包含 PRT 向量乘以每個頂點 >albedo。 如果這個輸出緩衝區是材質物件，則必須小心將材質的 >albedo 儲存為模擬緩衝區的相同解析度。 您可以在具有 [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)的 >albedo 上設定適當的解決方式，並套用材質裝訂邊區域（如果適用）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

ID3DXPRTEngine：： Computexxx 方法會計算輸出緩衝區，其中燈的信號尚未乘以 >albedo。 藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。

若要在呈現的光線模型中包含 >albedo，請在其中一個 Computexxx 方法之後呼叫此方法。

呼叫這個方法之前，應該先呼叫 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




