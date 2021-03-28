---
title: 介面和類別
description: 動態著色器連結使用高階著色器語言 (HLSL) 介面和類別，其語法類似于 c + + 的對應專案。
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376185"
---
# <a name="interfaces-and-classes"></a>介面和類別

動態著色器連結使用高階著色器語言 (HLSL) 介面和類別，其語法類似于 c + + 的對應專案。 這可讓著色器在編譯時期參考抽象介面實例，並在執行時間將這些實例的解決方案維持在應用程式的具體類別中。

下列各節將詳細說明如何設定著色器以使用介面和類別，以及如何在應用程式程式碼中初始化介面實例。

-   [宣告介面](#declaring-interfaces)
-   [宣告類別](#declaring-classes)
-   [著色器中的介面實例宣告](#interface-instance-declarations-in-a-shader)
-   [著色器中的類別實例宣告](#class-instance-declarations-in-a-shader)
-   [初始化應用程式中的介面實例](#initializing-interface-instances-in-an-application)
-   [相關主題](#related-topics)

## <a name="declaring-interfaces"></a>宣告介面

介面函式的方式類似于 c + + 中的抽象基類。 介面是在著色器中使用 interface 關鍵字宣告，而且只包含方法宣告。 在介面中宣告的方法，都是衍生自介面的任何類別中的虛擬方法。 衍生的類別必須執行介面中宣告的所有方法。 請注意，介面是宣告虛擬方法的唯一方法，不像 c + + 中的虛擬關鍵字，而類別 connot 宣告虛擬方法。

下列範例著色器程式碼會宣告兩個介面。


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a>宣告類別

類別的行為方式與 c + + 中的類別類似。 類別是以 class 關鍵字宣告，而且可以包含成員變數和方法。 類別可以繼承自零或一個類別以及零或多個介面。 類別必須針對其繼承鏈中的所有介面，或無法具現化類別，來實或繼承其執行。

下列範例著色器程式碼說明如何從介面和另一個類別衍生類別。


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a>著色器中的介面實例宣告

介面實例可做為類別實例的預留位置，以提供介面方法的執行。 使用介面的實例可讓著色器程式碼呼叫方法，而不需要知道將會叫用該方法的何種實作為。 著色器程式碼會針對它所定義的每個介面宣告一個或多個實例。 這些實例會以類似 c + + 基類指標的方式用於著色器程式碼中。

下列範例著色器程式碼說明如何宣告數個介面實例，並在著色器程式碼中使用它們。


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a>著色器中的類別實例宣告

每個將用來取代介面實例的類別，都必須宣告為常數緩衝區中的變數，或在執行時間使用 [**ID3D11ClassLinkage：： CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) 方法，由應用程式建立。 介面實例會指向應用程式程式碼中的類別實例。 類別實例可以在著色器程式碼中參考，如同任何其他變數，但衍生自介面的類別通常只會搭配介面實例使用，而且不會直接由著色器程式碼參考。

下列範例著色器程式碼說明如何宣告數個類別實例。


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a>初始化應用程式中的介面實例

介面實例會在應用程式程式碼中初始化，方法是將包含介面指派的動態連結陣列傳遞給其中一個 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader 方法。

若要建立動態連結陣列，請使用下列步驟

1.  使用 [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage)建立類別連結化物件。
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  建立將使用動態類別連結的著色器，並將類別連結化物件做為參數傳遞給著色器的 create 函式。
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  使用 [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect)函數來建立 [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)物件。
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  使用著色器反映物件，以使用 [**ID3D11ShaderReflection：： GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) 方法取得著色器中的介面實例數目。
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  建立夠大的陣列，以容納著色器中的介面實例數目。
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  使用 [**ID3D11ShaderReflection：： GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) 和 [**ID3D11ShaderReflectionVariable：： GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot)，判斷陣列中對應至每個介面實例的索引。
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  使用 [**ID3D11ClassLinkage：： GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance)，從著色器中的介面取得每個衍生自介面之類別物件的類別實例。
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  藉由設定動態連結陣列中的對應專案，將介面實例設定為類別實例。
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  將動態連結陣列做為參數傳遞至 SetShader 呼叫。
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>相關主題

[動態連結](overviews-direct3d-11-hlsl-dynamic-linking.md)