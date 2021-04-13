---
description: 設定3D 場景中的網格材質屬性。 使用這個方法來指定地下散佈參數。
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine：： SetMeshMaterials 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323251"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>ID3DXPRTEngine：： SetMeshMaterials 方法

設定3D 場景中的網格材質屬性。 使用這個方法來指定地下散佈參數。

## <a name="syntax"></a>語法


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppMaterials* \[在\]
</dt> <dd>

Type： **Const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

所需之網格材質屬性指標的位址。 請參閱 [**D3DXSHMATERIAL**](d3dxshmaterial.md)。

</dd> <dt>

*NumMeshes* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要在其上設定材質屬性之網格的索引。

</dd> <dt>

*NumChannels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要在網格中設定的色彩通道數目。 設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。 如果您想要變更此參數，請先使用另一種方法來設定 >albedo，例如 [**ID3DXPRTEngine：： SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) 或 [**ID3DXPRTEngine：： SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)。

</dd> <dt>

*bSetAlbedo* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，則會將網格的 >albedo 設定為 ppMaterials，並覆寫所有現有的材質和頂點 >albedo 值。 如果 **為 FALSE**，則會保留其他方法所設定的所有現有材質和頂點 >albedo 值;NumChannels 必須符合用來在 [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) 或 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)中建立緩衝區的 NumChannels 參數。

</dd> <dt>

*fLengthScale* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

相對於 1 mm cube 的3D 場景規模。 用於地下散佈計算。

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

 

 
