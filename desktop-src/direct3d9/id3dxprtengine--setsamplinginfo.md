---
description: 設定預先計算 radiance 傳輸 (PRT) 模擬器所使用的取樣屬性。
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine：： SetSamplingInfo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db15bc2120f90cf52aa4f3c41eccecc7d308cc8392ae368cd4423a90f218f6ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293362"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>ID3DXPRTEngine：： SetSamplingInfo 方法

設定預先計算 radiance 傳輸 (PRT) 模擬器所使用的取樣屬性。

## <a name="syntax"></a>語法


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumRays* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要在每個樣本上導向的光線數量。 必須大於零。

</dd> <dt>

*UseSphere* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，將會針對整個球體計算範例。 如果 **為 FALSE**，則會透過半球計算範例。

</dd> <dt>

*UseCosine* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE，則** 使用範例的余弦加權。 如果 UseCosine 和 UseSphere 都是 **TRUE**，方法將會失敗，而且會傳回錯誤。

</dd> <dt>

*適應性* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

必須為 **FALSE**。 彈性取樣目前未執行。

</dd> <dt>

*AdaptiveThresh* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、e \_ >notimpl、e \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
