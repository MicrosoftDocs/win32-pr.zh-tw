---
description: 此頁面將示範如何產生和使用效果。
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: '使用效果 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109884"
---
# <a name="using-an-effect-direct3d-9"></a>使用效果 (Direct3D 9) 

此頁面將示範如何產生和使用效果。 涵蓋的主題包括如何：

-   [建立效果](#create-an-effect)
-   [呈現效果](#render-an-effect)
-   [使用語義來尋找效果參數](#use-semantics-to-find-effect-parameters)
-   [使用控制碼有效率地取得和設定參數](#use-handles-to-get-and-set-parameters-efficiently)
-   [使用批註新增參數資訊](#add-parameter-information-with-annotations)
-   [共用效果參數](#share-effect-parameters)
-   [離線編譯效果](#compile-an-effect-offline)
-   [使用 Preshaders 改善效能](#improve-performance-with-preshaders)
-   [使用參數區塊來管理效果參數](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>建立效果

以下是建立從 [BasicHLSL 範例](../directx-sdk--august-2009-.md)取得之效果的範例。 建立偵錯工具著色器的效果建立程式碼是來自 **OnCreateDevice**：


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



此函式會採用下列引數：

-   裝置。
-   效果檔案的檔案名。
-   以 Null 終止的定義清單的指標，可在 \# 剖析著色器時使用。
-   使用者撰寫的 include 處理常式的選擇性指標。 每當處理器需要解析包含時，就會呼叫此處理程式 \# 。
-   著色器編譯旗標，可讓編譯器提示您瞭解如何使用著色器。 選項包括：
    -   如果正在編譯已知的良好著色器，則略過驗證。
    -   略過優化 (有時會在優化使) 更難進行調試時使用。
    -   要求要包含在著色器中的 debug 資訊，讓它可以進行調試。
-   效果集區。 如果有多個效果使用相同的記憶體集區指標，則效果中的全域變數會彼此共用。 如果不需要共用效果變數，記憶體集區可以設定為 **Null**。
-   新效果的指標。
-   可傳送驗證錯誤之緩衝區的指標。 在此範例中，參數已設為 **Null** 且未使用。

> [!Note]  
> 自2006年12月起的 SDK 起，DirectX 10 HLSL 編譯器現在是 DirectX 9 和 DirectX 10 中的預設編譯器。 請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。

 

## <a name="render-an-effect"></a>呈現效果

將效果狀態套用至裝置的呼叫順序為：

-   [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 設定使用中的技術。
-   [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 會設定主動傳遞。
-   [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) 會更新傳遞中任何 set 呼叫的變更。 這應該在任何繪製呼叫之前呼叫。
-   [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md) 結束傳遞。
-   [**ID3DXEffect：： End**](id3dxeffect--end.md) 結束使用中的技術。

效果轉譯程式碼也比對應的轉譯程式碼還簡單，而不會有效果。 以下是具有效果的轉譯程式碼：


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



轉譯迴圈包含查詢效果，以查看其中包含多少個傳遞，然後呼叫一項技術的所有階段。 您可以展開轉譯迴圈來呼叫多個技術，每個都有多個階段。

## <a name="use-semantics-to-find-effect-parameters"></a>使用語義來尋找效果參數

語義是附加至效果參數的識別碼，可讓應用程式搜尋參數。 參數最多隻能有一個語義。 語義位於冒號 (：在參數名稱之後 ) 。 例如：


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



如果您在未使用語義的情況下宣告效果全域變數，則會改為這樣：


```
float4x4 matWorldViewProj;
```



效果介面可以使用語義來取得特定效果參數的控制碼。 例如，下列範例會傳回矩陣的控制碼：


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



除了依語義名稱搜尋，效果介面還有許多其他方法可搜尋參數。

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>使用控制碼有效率地取得和設定參數

控點提供有效的方法來參考效果參數、技術、傳遞和具有效果的批註。 處理屬於 D3DXHANDLE) 類型的 (是字串指標。 傳遞至函式（例如 GetParameterxxx 或 GetAnnotationxxx）的控制碼可以是下列三種形式的其中一種：

-   函數所傳回的控制碼，例如 GetParameterxxx。
-   字串，其中包含參數、技術、傳遞或注釋的名稱。
-   控制碼設為 **Null**。

此範例會將控制碼傳回給已附加 WORLDVIEWPROJ 語義的參數：


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>使用批註新增參數資訊

批註是使用者特定的資料，可附加至任何技術、傳遞或參數。 批註是將資訊新增至個別參數的彈性方式。 您可以使用應用程式選擇的任何方式來讀回信息。 批註可以是任何資料類型，而且可以動態加入。 批註宣告是以角括弧分隔。 批註包含：

-   資料類型。
-   變數名稱。
-   等號 (=) 。
-   資料值。
-   結束分號 (; ) 。

比方說，這份檔中的上述兩個範例都包含這個批註：


```
texture Tex0 < string name = "tiger.bmp"; >;
```



批註會附加至材質物件，並指定應該用來初始化材質物件的材質檔。 批註不會初始化材質物件，它只是附加至變數的一段使用者資訊。 應用程式可以使用 [**ID3DXBaseEffect：： GetAnnotation**](id3dxbaseeffect--getannotation.md) 或 [**ID3DXBaseEffect：： GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) 來讀取注釋，以傳回字串。 應用程式也可以新增批註。

每個批註：

-   必須是數值或字串。
-   必須一律以預設值初始化。
-   可以與技術建立關聯 [，並將 (Direct3D 9) ](techniques-and-passes.md) 和最上層 [效果參數](/previous-versions/windows/desktop/ee417539(v=vs.85))傳遞。
-   可以使用 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)來寫入和讀取。
-   可以使用 [**ID3DXEffect**](id3dxeffect.md)新增。
-   無法在效果內部參考。
-   不能有子語義或子批註。

## <a name="share-effect-parameters"></a>共用效果參數

效果參數是在效果中宣告的所有非靜態變數。 這可能包括全域變數和批註。 您可以使用 "shared" 關鍵字宣告參數，然後使用效果集區來建立效果，以在不同效果之間共用效果參數。

效果集區包含共用效果參數。 集區的建立方式是呼叫 [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)，它會傳回 [**ID3DXEffectPool**](id3dxeffectpool.md) 介面。 建立效果時，可以將介面提供為任何 D3DXCreateEffectxxx 函數的輸入。 若要讓參數跨多個效果共用，參數在每個共用效果中都必須具有相同的名稱、類型和語義。


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



共用參數必須使用相同裝置的效果。 這會強制執行，以防止在不同裝置上共用裝置相依參數 (例如著色器或紋理) 。 只要釋放包含共用參數的效果，就會從集區中刪除參數。 如果不需要共用參數，則在建立效果時為效果集區提供 **Null** 。

複製的效果會使用與複製的效果相同的效果集區。 複製效果會產生效果的完整複本，包括全域變數、技術、傳遞和批註。

## <a name="compile-an-effect-offline"></a>離線編譯效果

您可以使用 [**D3DXCreateEffect**](d3dxcreateeffect.md)在執行時間編譯效果，也可以使用命令列編譯器工具 fxc.exe 離線編譯效果。 [CompiledEffect 範例](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx)中的效果包含頂點著色器、圖元著色器和一項技術：


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



使用 [效果編譯器工具](../direct3dtools/fxc.md) 來編譯 vs 1 1 的著色器時，會 \_ \_ 產生下列元件著色器指示：


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>使用 Preshaders 改善效能

Preshader 是藉由預先計算常數著色器運算式來提高著色器效率的技巧。 效果編譯器會自動從著色器的主體取出著色器計算，並在執行著色器之前的 CPU 上執行它們。 因此，preshaders 只會處理效果。 比方說，這兩個運算式可以在著色器之外進行評估，然後再執行。


```
mul(World,mul(View, Projection));
sin(time)
```



可以移動的著色器計算是與統一參數相關聯的計算;也就是說，每個頂點或圖元的計算都不會變更。 如果您使用效果，則效果編譯器會自動為您產生並執行 preshader;沒有可啟用的旗標。 Preshaders 可以減少每個著色器的指令數目，也可以減少著色器取用的常數暫存器數目。

將效果編譯器視為多處理器編譯器的一種，因為它會針對兩種類型的處理器編譯著色器程式碼： CPU 和 GPU。 此外，效果編譯器的設計目的是要將程式碼從 GPU 移到 CPU，進而改善著色器效能。 這非常類似于從迴圈中提取靜態運算式。 將位置從世界空間轉換成投射空間的著色器，以及複製材質座標在 HLSL 中看起來像這樣：


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



使用 [效果編譯器工具](../direct3dtools/fxc.md) 來編譯 vs 1 1 的著色器會 \_ \_ 產生下列元件指示：


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



這會使用大約14個插槽，並取用9個常數暫存器。 使用 preshader 時，編譯器會將靜態運算式移出著色器和 preshader。 使用 preshader 時，相同的著色器看起來像這樣：


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



效果會在執行著色器之前執行 preshader。 結果會與著色器效能增加的功能相同，因為每個頂點或圖元所需執行的指令數目 (，視著色) 器的類型而定，這可能會減少。 此外，著色器會使用較少的常數暫存器，做為將靜態運算式移至 preshader 的結果。 這表示，預先著色器先前受限於所需的常數暫存器數目，現在可能會進行編譯，因為它們需要較少的常數暫存器。 從 preshaders 得到5% 的效能和20% 的效能改進相當合理。

請記住，輸入常數與 preshader 中的輸出常數不同。 輸出 c1 與輸入 c1 暫存器不同。 寫入至 preshader 中的常數暫存器實際上會寫入對應的著色器輸入 (常數) 位置。


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



上述的 cmp 指令會讀取 preshader c1 值，而 mul 指令則會寫入至頂點著色器所使用的硬體著色器暫存器。

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>使用參數區塊來管理效果參數

參數區塊是作用中狀態變更的區塊。 參數區塊可以記錄狀態變更，以便稍後透過單一呼叫來套用。 藉由呼叫 [**ID3DXEffect：： BeginParameterBlock**](id3dxeffect--beginparameterblock.md)來建立參數區塊：


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



參數區塊可節省 API 呼叫所套用的四項變更。 呼叫 [**ID3DXEffect：： BeginParameterBlock**](id3dxeffect--beginparameterblock.md) 會開始記錄狀態變更。 [**ID3DXEffect：： EndParameterBlock**](id3dxeffect--endparameterblock.md) 會停止將變更新增至參數區塊，並傳回控制碼。 呼叫 [**ID3DXEffect：： ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)時，將會使用此控制碼。

在 [EffectParam 範例](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)中，參數區塊會套用於轉譯順序中：


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



參數區塊會在呼叫 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 之前，設定全部四個狀態變更的值。 參數區塊是使用單一 API 呼叫來設定多個狀態變更的便利方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影響](effects.md)
</dt> </dl>

 

 
