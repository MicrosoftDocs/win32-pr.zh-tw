---
description: 將材質轉譯至檔案，並將結果傳回至主機 asynchrnously。
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： RenderTextureAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41189637fd741d22fc566f913b25ddba1109854ed12a0336ffac899c10fd3147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405678"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： RenderTextureAsync 方法

將材質轉譯至檔案，並將結果傳回至主機 asynchrnously。

## <a name="syntax"></a>語法


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*textureId*   
要呈現之材質的識別碼。

*sliceIndex*   
要呈現之材質內的配量索引。

*formatOverride*   
色彩格式覆寫。

*降低*   

*上*   

*shaderFileName*   
COM 字串，其中包含著色器檔案的路徑名稱。

*numFloatShaderVars*   
浮點數著色器變數的數目

*count6 \_ shaderFloatVarName*   
COM 字串會寫入浮點著色器變數的名稱。

*count6 \_ shaderFloatVarValue*   
浮點著色器變數。

*numBoolShaderVars*   
布林著色器變數的數目。

*count9 \_ shaderBoolVarName*   
COM 字串會寫入布林著色器變數的名稱。

*count9 \_ shaderBoolVarValue*   
布林著色器變數。

*renderContentFileName*   
COM 字串，其中包含轉譯的材質寫入之檔案的路徑名稱。

*回檔*   
提供 IPixEngine5 回呼介面之物件的位址。

*requestCookie*   
可唯一識別要求的 cookie，而且可用來指示它被取消。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
