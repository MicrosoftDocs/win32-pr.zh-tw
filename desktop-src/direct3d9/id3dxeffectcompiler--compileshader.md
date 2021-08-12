---
description: 從包含一或多個函式的效果編譯著色器。
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler：： CompileShader 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1e42eec5cc9c5c90d1fa4e26c4ad38d611dce3ce0df933d76b1eb81d2534b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295874"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>ID3DXEffectCompiler：： CompileShader 方法

從包含一或多個函式的效果編譯著色器。

## <a name="syntax"></a>語法


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFunction* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

要編譯之函數的唯一識別碼。 此值不得為 **Null**。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pTarget* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

著色器設定檔的指標，此設定檔可決定著色器指令集。 如需可用的配置檔案清單，請參閱 [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) 或 [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) 。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

不同旗標所識別的編譯選項。 Direct3D 10 HLSL 編譯器現在是預設值。 如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。

</dd> <dt>

*ppShader* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含已編譯著色器的緩衝區。 編譯器著色器是 Dword 的陣列。 如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> <dt>

*ppErrorMsgs* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含至少發生第一個編譯錯誤訊息的緩衝區。 這包括對編譯器錯誤和高階語言編譯錯誤的影響。 如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> <dt>

*ppConstantTable* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

傳回 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面，這個介面可以用來存取著色器常數。 這個值可以是 **Null**。 如果您將應用程式編譯為大型位址感知 (也就是說，您可以使用/LARGEADDRESSAWARE 連結器選項來處理大於 2 GB 的位址) ，您無法使用此參數，而且必須將它設定為 **Null**。 相反地，您必須使用 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) 函式來取出內嵌于著色器中的著色器常數資料表。 在這個 **D3DXGetShaderConstantTableEx** 呼叫中，您必須將 **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** 旗標傳遞給 *Flags* 參數，以指定最多可存取 4 GB 的虛擬位址空間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。

如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。

如果方法失敗，傳回值將會是 E \_ 失敗。

## <a name="remarks"></a>備註

您可以針對頂點著色器、圖元著色器和紋理填滿功能指定目標。



| Targets                      | 函式                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| 頂點著色器目標 | vs \_ 1 \_ 1、vs \_ 2 \_ 0、vs \_ 2 \_ sw、vs \_ 3 \_ 0                               |
| 圖元著色器目標  | ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4、ps \_ 2 \_ 0、ps \_ 2 \_ sw、ps \_ 3 \_ 0 |
| 紋理填滿目標  | 德克薩斯州 \_ 0，德克薩斯州 \_ 1                                                          |



 

這個方法會從以類似 C 的語言撰寫的函式編譯著色器。 如需詳細資訊，請參閱 [HLSL](../direct3dhlsl/dx-graphics-hlsl.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
