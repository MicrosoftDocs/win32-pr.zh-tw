---
title: 'D3DCOMPILE 常數 (D3DCompiler) '
description: D3DCOMPILE 常數會指定編譯器如何編譯 HLSL 程式碼。
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196197"
---
# <a name="d3dcompile-constants"></a>D3DCOMPILE 常數

D3DCOMPILE 常數會指定編譯器如何編譯 HLSL 程式碼。

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE \_ DEBUG**
</dt> <dd> <dl> <dt>

 (1 << 0) 
</dt> <dt>



指示編譯器將 debug 檔案/行/型別/符號資訊插入輸出程式碼中。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ 略過 \_ 驗證**
</dt> <dd> <dl> <dt>

 (1 << 1) 
</dt> <dt>



指示編譯器不要針對已知的功能和條件約束來驗證產生的程式碼。 我們建議您只將此常數用於過去已成功編譯的著色器。 DirectX 一律會在著色器設定為裝置之前先進行驗證。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ 略過 \_ 優化**
</dt> <dd> <dl> <dt>

 (1 << 2) 
</dt> <dt>



指示編譯器在程式碼產生期間略過優化步驟。 我們建議您只針對 debug 用途設定這個常數。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE \_ PACK \_ 矩陣資料 \_ 列 \_ 主要**
</dt> <dd> <dl> <dt>

 (1 << 3) 
</dt> <dt>



指示編譯器針對著色器的輸入和輸出，以資料列主要順序封裝矩陣。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE \_ PACK \_ 矩陣資料 \_ 行 \_ 主要**
</dt> <dd> <dl> <dt>

 (1 << 4) 
</dt> <dt>



指示編譯器將資料行主要順序的矩陣封裝在著色器的輸入和輸出上。 這種類型的封裝通常更有效率，因為一系列的點積可以接著執行向量矩陣乘法。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE \_ 部分有效 \_ 位數**
</dt> <dd> <dl> <dt>

 (1 << 5) 
</dt> <dt>



指示編譯器以部分有效位數執行所有計算。 如果您設定這個常數，編譯的程式碼可能會在某些硬體上執行得更快。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ 強制 \_ VS \_ SOFTWARE \_ 無 \_ 選擇**
</dt> <dd> <dl> <dt>

 (1 << 6) 
</dt> <dt>



指示編譯器針對下一個最高的著色器設定檔編譯頂點著色器。 這個常數會開啟和優化的調試。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ 強制 \_ PS \_ 軟體 \_ 無 \_ OPT**
</dt> <dd> <dl> <dt>

 (1 << 7) 
</dt> <dt>



指示編譯器針對下一個最高的著色器設定檔編譯圖元著色器。 這個常數也會開啟和優化的調試。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ NO \_ PRESHADER**
</dt> <dd> <dl> <dt>

 (1 << 8) 
</dt> <dt>



指示編譯器停用 Preshaders。 如果您設定這個常數，編譯器不會提取用於評估的靜態運算式。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ 避免 \_ 流量 \_ 控制**
</dt> <dd> <dl> <dt>

 (1 << 9) 
</dt> <dt>



指示編譯器在可能的情況下不使用流程式控制制結構。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ 偏好 \_ 流程 \_ 控制**
</dt> <dd> <dl> <dt>

 (1 << 10) 
</dt> <dt>



指示編譯器盡可能使用流程式控制制結構。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ 啟用 \_ 嚴謹度**
</dt> <dd> <dl> <dt>

 (1 << 11) 
</dt> <dt>



強制執行嚴格的編譯，這可能不允許舊版語法。

根據預設，編譯器會在已被取代的語法上停用嚴謹度。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ 啟用 \_ 回溯 \_ 相容性**
</dt> <dd> <dl> <dt>

 (1 << 12) 
</dt> <dt>



指示編譯器啟用較舊的著色器，以編譯為 5 \_ 0 目標。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ 嚴謹度**
</dt> <dd> <dl> <dt>

 (1 << 13) 
</dt> <dt>



強制 IEEE strict 編譯。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ 優化 \_ LEVEL0**
</dt> <dd> <dl> <dt>

 (1 << 14) 
</dt> <dt>



指示編譯器使用最低的優化層級。 如果您設定這個常數，編譯器可能會產生較慢的程式碼，但會更快速地產生程式碼。 當您反復開發著色器時，請設定這個常數。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ 優化 \_ 級別1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



指示編譯器使用第二個最低的優化層級。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ 優化的 \_ 級別2**
</dt> <dd> <dl> <dt>

 ( (1 << 14) \| (1 << 15) ) 
</dt> <dt>



指示編譯器使用第二個最高的優化層級。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ 優化- \_ 3**
</dt> <dd> <dl> <dt>

 (1 << 15) 
</dt> <dt>



指示編譯器使用最高的優化層級。 如果您設定這個常數，編譯器會產生最佳的程式碼，但可能需要花費很長的時間才能完成。 當效能是最重要的因素時，請將此常數設定為最終的應用程式組建。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE \_ 警告 \_ 為 \_ 錯誤**
</dt> <dd> <dl> <dt>

 (1 << 18) 
</dt> <dt>



指示編譯器在編譯著色器程式碼時，將所有警告視為錯誤。 我們建議您針對新的著色器程式碼使用這個常數，如此您就可以解決所有警告，並減少難以找到的程式碼缺失數目。


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE \_ 資源 \_ 可能是 \_ 別名**
</dt> <dd> <dl> <dt>

 (1 << 19) 
</dt> <dt>



指示編譯器假設未排序的存取視圖 (UAVs) 和著色器資源檢視 (SRVs) 可能是 cs \_ 5 0 的別名 \_ 。

> [!Note]  
> 從 D3dcompiler47.dll 開始，這個編譯器常數是新的 \_ 。

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE 啟用未系結的 \_ \_ 描述元 \_ \_ 資料表**
</dt> <dd> <dl> <dt>

 (1 << 20) 
</dt> <dt>



指示編譯器啟用未系結的描述中繼資料表。

> [!Note]  
> 從 D3dcompiler47.dll 開始，這個編譯器常數是新的 \_ 。

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE 所有系結的 \_ \_ 資源 \_**
</dt> <dd> <dl> <dt>

 (1 << 21) 
</dt> <dt>



指示編譯器以確保所有資源都已系結。

> [!Note]  
> 從 D3dcompiler47.dll 開始，這個編譯器常數是新的 \_ 。

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DCompiler。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DCompiler 常數](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





