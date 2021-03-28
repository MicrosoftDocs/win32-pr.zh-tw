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
# <a name="interfaces-and-classes"></a><span data-ttu-id="a345f-103">介面和類別</span><span class="sxs-lookup"><span data-stu-id="a345f-103">Interfaces and classes</span></span>

<span data-ttu-id="a345f-104">動態著色器連結使用高階著色器語言 (HLSL) 介面和類別，其語法類似于 c + + 的對應專案。</span><span class="sxs-lookup"><span data-stu-id="a345f-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="a345f-105">這可讓著色器在編譯時期參考抽象介面實例，並在執行時間將這些實例的解決方案維持在應用程式的具體類別中。</span><span class="sxs-lookup"><span data-stu-id="a345f-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="a345f-106">下列各節將詳細說明如何設定著色器以使用介面和類別，以及如何在應用程式程式碼中初始化介面實例。</span><span class="sxs-lookup"><span data-stu-id="a345f-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="a345f-107">宣告介面</span><span class="sxs-lookup"><span data-stu-id="a345f-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="a345f-108">宣告類別</span><span class="sxs-lookup"><span data-stu-id="a345f-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="a345f-109">著色器中的介面實例宣告</span><span class="sxs-lookup"><span data-stu-id="a345f-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="a345f-110">著色器中的類別實例宣告</span><span class="sxs-lookup"><span data-stu-id="a345f-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="a345f-111">初始化應用程式中的介面實例</span><span class="sxs-lookup"><span data-stu-id="a345f-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="a345f-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="a345f-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="a345f-113">宣告介面</span><span class="sxs-lookup"><span data-stu-id="a345f-113">Declaring interfaces</span></span>

<span data-ttu-id="a345f-114">介面函式的方式類似于 c + + 中的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="a345f-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="a345f-115">介面是在著色器中使用 interface 關鍵字宣告，而且只包含方法宣告。</span><span class="sxs-lookup"><span data-stu-id="a345f-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="a345f-116">在介面中宣告的方法，都是衍生自介面的任何類別中的虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="a345f-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="a345f-117">衍生的類別必須執行介面中宣告的所有方法。</span><span class="sxs-lookup"><span data-stu-id="a345f-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="a345f-118">請注意，介面是宣告虛擬方法的唯一方法，不像 c + + 中的虛擬關鍵字，而類別 connot 宣告虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="a345f-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="a345f-119">下列範例著色器程式碼會宣告兩個介面。</span><span class="sxs-lookup"><span data-stu-id="a345f-119">The following example shader code declares two interfaces.</span></span>


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



## <a name="declaring-classes"></a><span data-ttu-id="a345f-120">宣告類別</span><span class="sxs-lookup"><span data-stu-id="a345f-120">Declaring Classes</span></span>

<span data-ttu-id="a345f-121">類別的行為方式與 c + + 中的類別類似。</span><span class="sxs-lookup"><span data-stu-id="a345f-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="a345f-122">類別是以 class 關鍵字宣告，而且可以包含成員變數和方法。</span><span class="sxs-lookup"><span data-stu-id="a345f-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="a345f-123">類別可以繼承自零或一個類別以及零或多個介面。</span><span class="sxs-lookup"><span data-stu-id="a345f-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="a345f-124">類別必須針對其繼承鏈中的所有介面，或無法具現化類別，來實或繼承其執行。</span><span class="sxs-lookup"><span data-stu-id="a345f-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="a345f-125">下列範例著色器程式碼說明如何從介面和另一個類別衍生類別。</span><span class="sxs-lookup"><span data-stu-id="a345f-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


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



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="a345f-126">著色器中的介面實例宣告</span><span class="sxs-lookup"><span data-stu-id="a345f-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="a345f-127">介面實例可做為類別實例的預留位置，以提供介面方法的執行。</span><span class="sxs-lookup"><span data-stu-id="a345f-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="a345f-128">使用介面的實例可讓著色器程式碼呼叫方法，而不需要知道將會叫用該方法的何種實作為。</span><span class="sxs-lookup"><span data-stu-id="a345f-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="a345f-129">著色器程式碼會針對它所定義的每個介面宣告一個或多個實例。</span><span class="sxs-lookup"><span data-stu-id="a345f-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="a345f-130">這些實例會以類似 c + + 基類指標的方式用於著色器程式碼中。</span><span class="sxs-lookup"><span data-stu-id="a345f-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="a345f-131">下列範例著色器程式碼說明如何宣告數個介面實例，並在著色器程式碼中使用它們。</span><span class="sxs-lookup"><span data-stu-id="a345f-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


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



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="a345f-132">著色器中的類別實例宣告</span><span class="sxs-lookup"><span data-stu-id="a345f-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="a345f-133">每個將用來取代介面實例的類別，都必須宣告為常數緩衝區中的變數，或在執行時間使用 [**ID3D11ClassLinkage：： CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) 方法，由應用程式建立。</span><span class="sxs-lookup"><span data-stu-id="a345f-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="a345f-134">介面實例會指向應用程式程式碼中的類別實例。</span><span class="sxs-lookup"><span data-stu-id="a345f-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="a345f-135">類別實例可以在著色器程式碼中參考，如同任何其他變數，但衍生自介面的類別通常只會搭配介面實例使用，而且不會直接由著色器程式碼參考。</span><span class="sxs-lookup"><span data-stu-id="a345f-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="a345f-136">下列範例著色器程式碼說明如何宣告數個類別實例。</span><span class="sxs-lookup"><span data-stu-id="a345f-136">The following example shader code illustrates declaring several class instances.</span></span>


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



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="a345f-137">初始化應用程式中的介面實例</span><span class="sxs-lookup"><span data-stu-id="a345f-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="a345f-138">介面實例會在應用程式程式碼中初始化，方法是將包含介面指派的動態連結陣列傳遞給其中一個 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader 方法。</span><span class="sxs-lookup"><span data-stu-id="a345f-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="a345f-139">若要建立動態連結陣列，請使用下列步驟</span><span class="sxs-lookup"><span data-stu-id="a345f-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="a345f-140">使用 [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage)建立類別連結化物件。</span><span class="sxs-lookup"><span data-stu-id="a345f-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="a345f-141">建立將使用動態類別連結的著色器，並將類別連結化物件做為參數傳遞給著色器的 create 函式。</span><span class="sxs-lookup"><span data-stu-id="a345f-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="a345f-142">使用 [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect)函數來建立 [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)物件。</span><span class="sxs-lookup"><span data-stu-id="a345f-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="a345f-143">使用著色器反映物件，以使用 [**ID3D11ShaderReflection：： GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) 方法取得著色器中的介面實例數目。</span><span class="sxs-lookup"><span data-stu-id="a345f-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="a345f-144">建立夠大的陣列，以容納著色器中的介面實例數目。</span><span class="sxs-lookup"><span data-stu-id="a345f-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="a345f-145">使用 [**ID3D11ShaderReflection：： GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) 和 [**ID3D11ShaderReflectionVariable：： GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot)，判斷陣列中對應至每個介面實例的索引。</span><span class="sxs-lookup"><span data-stu-id="a345f-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="a345f-146">使用 [**ID3D11ClassLinkage：： GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance)，從著色器中的介面取得每個衍生自介面之類別物件的類別實例。</span><span class="sxs-lookup"><span data-stu-id="a345f-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="a345f-147">藉由設定動態連結陣列中的對應專案，將介面實例設定為類別實例。</span><span class="sxs-lookup"><span data-stu-id="a345f-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="a345f-148">將動態連結陣列做為參數傳遞至 SetShader 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a345f-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="a345f-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="a345f-149">Related topics</span></span>

[<span data-ttu-id="a345f-150">動態連結</span><span class="sxs-lookup"><span data-stu-id="a345f-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)