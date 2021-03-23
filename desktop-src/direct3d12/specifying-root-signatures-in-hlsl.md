---
title: 在 HLSL 中指定根簽章
description: 在 HLSL 著色器模型5.1 中指定根簽章是在 c + + 程式碼中指定它們的替代方法。
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548353"
---
# <a name="specifying-root-signatures-in-hlsl"></a>在 HLSL 中指定根簽章

在 HLSL 著色器模型5.1 中指定根簽章是在 c + + 程式碼中指定它們的替代方法。

-   [HLSL 根簽章的範例](#an-example-hlsl-root-signature)
    -   [根簽章版本1。0](#root-signature-version-10)
    -   [根簽章版本1。1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [根常數](#root-constants)
-   [可見度](#visibility)
-   [根層級 CBV](#root-level-cbv)
-   [根目錄層級 SRV](#root-level-srv)
-   [根層級 UAV](#root-level-uav)
-   [描述項資料表](#descriptor-table)
-   [靜態取樣器](#static-sampler)
-   [編譯 HLSL 的根簽章](#compiling-an-hlsl-root-signature)
-   [使用 FXC.EXE 編譯器操作根簽章](#manipulating-root-signatures-with-the-fxc-compiler)
-   [注意事項](#notes)
-   [相關主題](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>HLSL 根簽章的範例

根簽章可以在 HLSL 中指定為字串。 字串包含以逗號分隔的子句集合，其描述根簽章構成元件。 在 (PSO) 的任何一個管線狀態物件的著色器中，根簽章應該相同。 請看以下範例：

### <a name="root-signature-version-10"></a>根簽章版本1。0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

### <a name="root-signature-version-11"></a>根簽章版本1。1

[根簽章版本 1.1](root-signature-version-1-1.md) 可針對根簽章描述元和資料啟用驅動程式優化。

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

這項定義會提供下列根簽章，請注意：

-   使用預設參數。
-   b0 和 (b0，space = 1) 不會衝突
-   只有幾何著色器可以看到 u0
-   u4 和 u5 的別名為堆積中的相同描述元

![使用高階著色器語言指定的根簽章](images/hlsl-root-signature.png)

HLSL 根簽章語言會與 c + + 根簽章 Api 緊密對應，且具有相當的表達能力。 根簽章會指定為一系列的子句，並以逗號分隔。 子句順序很重要，因為剖析的順序會決定根簽章中的位置位置。 每個子句都接受一個或多個具名引數。 但參數的順序並不重要。

## <a name="rootflags"></a>RootFlags

選擇性 *RootFlags* 子句會採用 0 (預設值來指出沒有旗標) ，或透過或 ' ' 運算子連接的一或多個預先定義的根旗標值 \| 。 允許的根旗標值是透過 [**D3D12 \_ 根簽章 \_ \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)來定義。

例如：

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>根常數

*RootConstants* 子句會指定根簽章中的根常數。 有兩個必要參數： *num32BitConstants* 和 *bReg* (註冊對應到 *Cbuffer* 的 c + + api) 中的 *BaseShaderRegister* 。 C + + Api 中 (*RegisterSpace* 的空間) 和 *(c* + +) 參數中的參數都是選擇性的，而預設值為：

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

例如：

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>可見性

可見度是選擇性參數，可具有 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)的其中一個值。

著色器 \_ 可見度全都會將 \_ 根引數廣播到所有著色器。 在某些硬體上，這不會產生任何費用，但在其他硬體上，將資料分支至所有著色器階段會有成本。 設定其中一個選項（例如著色器 \_ 可見度 \_ 頂點）會將根引數限制為單一著色器階段。

將根引數設定為單一著色器階段，可讓您在不同階段使用相同的系結名稱。 例如，和 SRV 系結的 SRV 系結將 `t0,SHADER_VISIBILITY_VERTEX` `t0,SHADER_VISIBILITY_PIXEL` 會是有效的。 但是，如果其中一個系結的可見度設定為，根簽章將 `t0,SHADER_VISIBILITY_ALL` 會無效。

## <a name="root-level-cbv"></a>根層級 CBV

`CBV` (常數緩衝區 view) 子句會指定根層級的常數緩衝區 b 註冊 Reg 專案。 請注意，這是純量專案;您無法指定根層級的範圍。

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>根目錄層級 SRV

`SRV` (著色器資源檢視) 子句會指定根層級的 SRV t a t a t a t a t a t a t a 請注意，這是純量專案;您無法指定根層級的範圍。

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>根層級 UAV

`UAV` (未排序的存取 view) 子句會指定根層級的 UAV u 註冊 Reg 專案。 請注意，這是純量專案;您無法指定根層級的範圍。

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

例如：

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>描述項資料表

`DescriptorTable`子句本身是以逗號分隔的描述元表子句清單，以及選擇性的可見度參數。 *DescriptorTable* 子句包括 CBV、SRV、UAV 和取樣器。 請注意，其參數與根層級子句的參數不同。

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

描述中繼資料表 `CBV` 有下列語法：

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

例如：

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

強制參數 *bReg* 指定 cbuffer 範圍的起始登錄。 *NumDescriptors* 參數會指定連續 cbuffer 範圍中的描述元數目;預設值為1。 ` [Reg, Reg + numDescriptors - 1]`當 *numDescriptors* 為數字時，專案會宣告 cbuffer 範圍。 如果 *numDescriptors* 等於「未系結」，則範圍為 `[Reg, UINT_MAX]` ，這表示應用程式必須確定它未參考超出範圍的區域。 *Offset* 欄位代表 c + + api 中的 *OffsetInDescriptorsFromTableStart* 參數，也就是從資料表開頭開始，) 描述項中 (的位移。 如果位移設定為描述 \_ \_ 項範圍位移 \_ 附加 (預設) ，則表示範圍是緊接在先前的範圍之後。 但是，輸入特定位移可讓範圍彼此重迭，允許註冊別名。

描述中繼資料表 `SRV` 有下列語法：

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

這與描述項資料表專案類似 `CBV` ，不同之處在于指定的範圍適用于著色器資源檢視。

描述中繼資料表 `UAV` 有下列語法：

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

這與描述項資料表專案類似 `CBV` ，不同之處在于指定的範圍適用于未排序的存取視圖。

描述中繼資料表 `Sampler` 有下列語法：

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

這類似于描述中繼資料表 `CBV` 專案，但指定的範圍適用于著色器取樣器。 請注意，取樣器無法與相同描述項資料表中的其他類型的描述項混合 (，因為它們位於不同的描述項堆積) 中。

## <a name="static-sampler"></a>靜態取樣器

靜態取樣器代表 [**D3D12 \_ 靜態取樣 \_ 器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構。 *StaticSampler* 的必要參數是純量、取樣器 s-註冊 Reg。其他參數則是選擇性的，預設值如下所示。 大部分的欄位都接受一組預先定義的列舉。

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

例如：

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

參數選項與 c + + API 呼叫非常類似，但 *邊框* 除外，只限于 HLSL 中的列舉。

篩選欄位可以是 [**D3D12 \_ 篩選準則**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)的其中一個。

[位址] 欄位可以是 [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)的其中一種。

比較函數可以是 [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)的其中一個。

[框線色彩] 欄位可以是 [**D3D12 \_ 靜態 \_ 框線 \_ 色彩**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color)的其中一個。

可見度可以是 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)的其中之一。

## <a name="compiling-an-hlsl-root-signature"></a>編譯 HLSL 的根簽章

有兩種機制可編譯 HLSL 的根簽章。 首先，您可以使用下列範例中的 *RootSignature* 屬性，將根簽章字串附加至特定著色器 (在下列範例中，使用 **MyRS1** 進入點) ：

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

編譯器會建立並驗證著色器的根簽章 blob，並將其與著色器位元組程式碼一起內嵌到著色器 blob 中。 編譯器支援著色器模型5.0 和更新版本的根簽章語法。 如果根簽章內嵌于著色器模型5.0 著色器中，而且該著色器會傳送至 D3D11 執行時間（而不是 D3D12），則 D3D11 會以無訊息方式忽略根簽章部分。

另一種機制是建立獨立的根簽章 blob，可能會使用大量著色器來重複使用它，以節省空間。 [效果編譯器工具](/windows/desktop/direct3dtools/fxc) (fxc.exe) 支援 **rootsig \_ 1 \_ 0** 和 **rootsig \_ 1 \_ 1** 著色器模型。 定義字串的名稱是透過一般的/E 引數所指定。 例如：

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

請注意，根簽章字串定義也可以在命令列上傳遞，例如/D MyRS1 = "..."。

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>使用 FXC.EXE 編譯器操作根簽章

FXC.EXE 編譯器會從 HLSL 來源檔案建立著色器位元組程式碼。 此編譯器有許多選擇性參數，請參閱 [效果編譯器工具](/windows/desktop/direct3dtools/fxc)。

為了管理 HLSL 撰寫的根簽章，下表提供使用 FXC.EXE 的一些範例。



| 線條 | 命令列                                                                 | 描述                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | 編譯圖元著色器5.1 目標的著色器，著色器來源位於 shaderWithRootSig. hlsl 檔案中，其中包含根簽章。 著色器和根簽章會編譯為 rs1. fxo 二進位檔案中的個別 blob。    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | 從行1建立的檔案中解壓縮根簽章，讓 rs1 檔案只包含根簽章。                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | 從行1建立的檔案中移除根簽章，因此 rs1 fxo 檔案包含沒有根簽章的著色器。                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | 將位於個別檔案中的著色器和根簽章合併為包含這兩個 blob 的二進位檔案。 在此範例中，rs1 會與行1中的 rs1. fx0 相同。                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | 從可能包含不只是根簽章的來源，建立獨立的根簽章二進位檔案。 請注意 rootsig \_ 1 \_ 0 目標，而該 RS1 是根簽章的名稱 (\# 在 HLSL 檔中定義) 宏字串。 |



 

透過 FXC.EXE 提供的功能也可透過程式設計的方式使用 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) 函式。 此呼叫會使用根簽章或獨立的根簽章來編譯著色器 (設定 rootsig \_ 1 \_ 0 目標) 。 [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) 和 [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) 可以解壓縮根簽章，並將其附加至現有的 blob。D3D \_ blob \_ 根簽章 \_ 用來指定根簽章 blob 元件類型。 [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) 會使用 \_ \_ 從 blob) 的 D3DCOMPILER 帶根簽章旗標， (移除根簽章 \_ 。

## <a name="notes"></a>備註

> [!Note]  
> 雖然強烈建議您以離線編譯著色器，但如果著色器必須在執行時間編譯，請參閱 [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)的備註。

 

> [!Note]  
> 現有的 HLSL 資產不需要變更，即可處理要搭配它們使用的根簽章。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 HLSL 5.1 的動態索引](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> <dt>

[HLSL 中的資源系結](resource-binding-in-hlsl.md)
</dt> <dt>

[根簽章](root-signatures.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[著色器指定的樣板參考值](shader-specified-stencil-reference-value.md)
</dt> <dt>

[具類型的未排序存取視圖載入](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 