---
description: D3DXSHADER 旗標是用來剖析、編譯或組合著色器。
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: 'D3DXSHADER 旗標 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 031ae23301b78a9cced683551c9d7220aa66f7e0a48b504fe1a93721fd8d6a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849778"
---
# <a name="d3dxshader-flags"></a>D3DXSHADER 旗標

**D3DXSHADER** 旗標是用來剖析、編譯或組合著色器。

**剖析器旗標**

只有當您建立效果編譯器時，效果系統才會使用剖析時間旗標 (效果編譯) 。 例如，您可以使用 **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** 建立編譯器物件，然後使用不同的編譯器旗標重複使用該編譯器物件來產生特製化程式碼。



| 常數                                                                                                                                                                                                                   | 描述                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | 除非明確指定，否則矩陣將會以資料行主要順序封裝 (每個向量都會在與著色器之間傳遞的單一資料行) 。 這通常更有效率，因為它允許使用一連串的點乘積來執行向量矩陣乘法。<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | 除非明確指定，否則矩陣將會以資料列主要順序封裝 (每個向量在傳遞至或從著色器傳遞至或時，都會在單一資料列) 。<br/>                                                                                                                                        |



**編譯器旗標**

DirectX 10 HLSL 編譯器現在是預設的編譯器。 請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。

下表詳細說明 Direct3D 9 和 Direct3D 10 中可用的旗標。 旗標的值是對等的 fxc.exe 選項。



| 常數/值                                                                                                                                                                                                                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_避免 \_ 流量 \_ 控制**</dt> <dt>/Gfa</dt> </dl>                                     | 這是編譯器的提示，可避免使用流程式控制制指令。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_DEBUG**</dt> <dt>/zi</dt> </dl>                                                                               | 在著色器編譯期間插入 debug 檔案名、行號和類型和符號資訊。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_啟用 \_ 回溯 \_ 相容性**</dt> <dt>/Gec</dt> </dl> | 將 ps \_ 1 \_ x 著色器編譯為 ps \_ 2 \_ 0。 指定 ps \_ 1 \_ x 目標的效果會改為在 ps \_ 2 \_ 0 目標上編譯，因為這是 DirectX 10 隨附的著色器編譯器版本所支援的最小著色器版本。 搭配較高層級的編譯目標使用時，此旗標不會有任何作用。<br/> Direct3D 9-否<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_強制 \_ PS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | 強制編譯器針對圖元著色器的下一個最高可用軟體目標進行編譯。 此旗標也會關閉優化並在上進行調試。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_強制 \_ VS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | 強制編譯器針對頂點著色器的下一個最高可用軟體目標進行編譯。 此旗標也會關閉優化並在上進行調試。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_IEEE \_ 嚴謹度**</dt> <dt>/Gis</dt> </dl>                                               | 停用可能導致編譯的著色器程式的輸出與使用 DirectX 9 著色器編譯器編譯之程式的輸出不同的優化，因為浮點數學錯誤的精確度很小。<br/> Direct3D 9-否<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_沒有 \_ PRESHADER**</dt> <dt>/Op</dt> </dl>                                                         | 停用 preshaders。 編譯器不會提取靜態運算式以進行主機 CPU 的評估。 此外，編譯獨立函式時，編譯器不會 loft 任何運算式。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_優化 \_ LEVEL0**</dt> <dt>/O0</dt> </dl>                                    | 最低優化層級。 可能會產生較慢的程式碼，但會更快完成。 這在高度反復的著色器開發週期中可能很有用。<br/> Direct3D 9-否<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_優化 \_ 級別**</dt>1 <dt>/O1</dt> </dl>                                    | 第二個最低優化層級。<br/> Direct3D 9-否<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_優化的 \_ 級別**</dt> <dt>/O2</dt> </dl>                                    | 第二個最高的優化層級。<br/> Direct3D 9-否<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_優化 \_ 3-3**</dt> <dt>/O3</dt> </dl>                                    | 最高的優化層級。 會產生最佳的程式碼，但可能需要花費很長的時間才能完成。 這適用于應用程式的最終組建，其中效能是最重要的因素。<br/> Direct3D 9-否<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_PARTIALPRECISION**</dt> <dt>/Gpp</dt> </dl>                                             | 強制產生的著色器中的所有計算都在部分有效位數發生。 這可能會導致在某些硬體上更快速地評估著色器。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_偏好 \_ 流程 \_ 控制**</dt> <dt>/Gfp</dt> </dl>                                  | 這是編譯器偏好使用流程式控制制指示的提示。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_SKIPOPTIMIZATION**</dt> <dt>/od</dt> </dl>                                              | 指示編譯器在程式碼產生期間略過優化步驟。 除非您嘗試找出程式碼中的問題，而且您懷疑編譯器，否則不建議使用此選項。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_SKIPVALIDATION**</dt> <dt>/Vd</dt> </dl>                                                    | 請勿針對已知的功能和條件約束來驗證產生的程式碼。 只有在編譯已知可運作的著色器時，才建議使用這個選項 (也就是在沒有此選項的情況下編譯過的著色器) 。 著色器一律會在設定為裝置之前，由執行時間進行驗證。<br/> Direct3D 9-是<br/> Direct3D 10-是<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_使用 \_ 舊版 \_ D3DX9 \_ 31 \_ DLL**</dt> <dt>/ld</dt> </dl>                     | 啟用原始 Direct3D 9 HLSL 編譯器的使用。 OCT2006 \_ d3dx9 \_ 31 \_x86.cab 或 OCT2006 \_ d3dx9 \_ 31 \_x64.cab 必須包含在應用程式可轉散發套件中。 您必須使用此旗標來編譯 ps \_ 1 \_ x 著色器，而不使用向 ps 2 0 的提升旗標 \_ \_ 。 在取得 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) 介面時指定此旗標，會導致後續透過此物件呼叫 [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) 和 [**CompileShader**](id3dxeffectcompiler--compileshader.md) ，以使用舊版編譯器。<br/> Direct3D 9-是<br/> Direct3D 10-否<br/> |



**組合器旗標**

效果系統會使用組合器旗標來優化著色器和效果元件程式碼。



| 常數                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> </dl>                                                          | 在著色器編譯期間插入 debug 檔案名、行號和類型和符號資訊。<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> </dl> | 強制編譯器針對圖元著色器的下一個最高可用軟體目標進行編譯。 此旗標也會關閉優化並在上進行調試。<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> </dl> | 強制編譯器針對頂點著色器的下一個最高可用軟體目標進行編譯。 此旗標也會關閉優化並在上進行調試。<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | 請勿針對已知的功能和條件約束來驗證產生的程式碼。 只有在編譯已知可運作的著色器時，才建議使用這個選項 (也就是在沒有此選項的情況下編譯過的著色器) 。 著色器一律會在設定為裝置之前，由執行時間進行驗證。<br/> |



## <a name="remarks"></a>備註

當下列函式呼叫時，效果系統將會使用剖析器 **旗標** ：

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

結果系統會在下列函式呼叫時使用 **編譯器旗標** ：

-   [**D3DXCompileShader**](d3dxcompileshader.md) (或 [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) 或 [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)) 
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (或 [**CompileShader**](id3dxeffectcompiler--compileshader.md)) 

此外，您可以藉由呼叫 [**D3DXCreateEffect**](d3dxcreateeffect.md) (或 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)或 [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)) 來建立效果，以使用 **編譯器旗標**。

-   如果您傳入未編譯的 fx 檔案，效果系統將會在編譯期間使用旗標輸入參數。
-   如果您傳入已編譯的效果，效果系統將會忽略編譯器旗標，因為它們不需要載入效果。

結果系統會在下列函式呼叫時使用組合器 **旗標** ：

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

將 **編譯器旗標** 或組合器 **旗標** 套用至不正確的 API 將會導致著色器驗證失敗。 使用 DirectX Error Lookup 工具 (DXErr.exe) ，檢查來自函式的 Direct3D 錯誤碼傳回值，以協助追蹤此錯誤。 您可以從 DirectX SDK 取得 DXErr.exe 並瞭解它的相關資訊。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 常數](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
