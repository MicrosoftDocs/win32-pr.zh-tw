---
description: 從記憶體建立效果。
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: D3DX10CreateEffectFromMemory 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 3bcc32e94d6329d42edd27f1daf39e40d28b71ba65cc32fd88d4ae3951d5012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989238"
---
# <a name="d3dx10createeffectfrommemory-function"></a>D3DX10CreateEffectFromMemory 函式

從記憶體建立效果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

記憶體中效果的指標。

</dd> <dt>

*DataLength* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

記憶體中效果的大小。

</dd> <dt>

*pSrcFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

記憶體中的效果檔案名。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。 此參數可以是 **Null**。

</dd> <dt>

*pProfile* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md)或著色器模型的字串。

</dd> <dt>

*HLSLFlags* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

HLSL 編譯選項 (參閱 [D3D10 \_ 著色器常數](d3d10-shader.md)) 。

</dd> <dt>

*FXFlags* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

效果編譯選項 (查看 [D3D10 \_ 效果常數](d3d10-effect.md)) 。

</dd> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

裝置的指標 (查看將使用這些資源的 [**ID3D10Device 介面**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) 。

</dd> <dt>

*pEffectPool* \[在\]
</dt> <dd>

類型： **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***

效果集區的指標 (查看 [**ID3D10EffectPool 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) ，以便在效果之間共用變數。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。 使用 **Null** 來指定此函式必須等到完成後才會傳回。

</dd> <dt>

*ppEffect* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***

效果的指標位址 (查看所建立的 [**ID3D10Effect 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) 。

</dd> <dt>

*ppErrors* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

記憶體指標的位址 (查看包含效果編譯錯誤（如果有的話）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。

</dd> <dt>

*pHResult* \[擴展\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。 如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Async。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
