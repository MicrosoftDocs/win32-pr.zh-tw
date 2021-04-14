---
description: 材質描述多邊形如何反映燈光，或看似在3D 場景中發出燈光。
ms.assetid: vs|directx_sdk|~\materials.htm
title: Direct3D 9) 的教材 (
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552269"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="79363-103">Direct3D 9) 的教材 (</span><span class="sxs-lookup"><span data-stu-id="79363-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="79363-104">材質描述多邊形如何反映燈光，或看似在3D 場景中發出燈光。</span><span class="sxs-lookup"><span data-stu-id="79363-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="79363-105">材質屬性會詳細說明材質的擴散反映、環境反映、光線排放和高光特性。</span><span class="sxs-lookup"><span data-stu-id="79363-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="79363-106">Direct3D 會使用 [**D3DMATERIAL9**](d3dmaterial9.md) 結構來攜帶所有材質屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="79363-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="79363-107">除了反射屬性之外，每個屬性都會描述為 RGBA 色彩，其代表指定之光線類型的紅色、綠色和藍色部分，以及 Alpha 混色因數。</span><span class="sxs-lookup"><span data-stu-id="79363-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="79363-108">擴散和環境反映</span><span class="sxs-lookup"><span data-stu-id="79363-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="79363-109">[**D3DMATERIAL9**](d3dmaterial9.md)結構的擴散和環境成員會描述材質如何反映場景中的環境和擴散燈。</span><span class="sxs-lookup"><span data-stu-id="79363-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="79363-110">因為大部分的場景所包含的擴散速度遠高於環境光線，所以擴散反映在決定色彩方面扮演最大的部分。</span><span class="sxs-lookup"><span data-stu-id="79363-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="79363-111">此外，由於擴散燈的方向，擴散光的發生角度會影響反映的整體濃度。</span><span class="sxs-lookup"><span data-stu-id="79363-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="79363-112">當光線將頂點平行至頂點正常時，擴散反映會很大。</span><span class="sxs-lookup"><span data-stu-id="79363-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="79363-113">當角度增加時，擴散反映的效果會降低。</span><span class="sxs-lookup"><span data-stu-id="79363-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="79363-114">反射的光線量是連入燈光與頂點法線之間的角度余弦值，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="79363-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![反映的光線量圖](images/incident.png)

<span data-ttu-id="79363-116">環境反映（像是環境燈）是 nondirectional。</span><span class="sxs-lookup"><span data-stu-id="79363-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="79363-117">環境反映對轉譯物件的明顯色彩會有較小的影響，但它會影響整體的色彩，而且在輕微或無擴散光線反映材質時，最明顯。</span><span class="sxs-lookup"><span data-stu-id="79363-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="79363-118">使用 D3DRS 環境旗標呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，以針對場景的環境光源來影響材質的環境反映 \_ 。</span><span class="sxs-lookup"><span data-stu-id="79363-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="79363-119">擴散和環境反映會一起運作，以判斷物件的已知色彩，且通常是相同的值。</span><span class="sxs-lookup"><span data-stu-id="79363-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="79363-120">例如，若要轉譯藍色 crystalline 物件，您可以建立只反映擴散和環境光源之藍色元件的材質。</span><span class="sxs-lookup"><span data-stu-id="79363-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="79363-121">放在具有白色燈光的房間時，crystal 會顯示為藍色。</span><span class="sxs-lookup"><span data-stu-id="79363-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="79363-122">不過，在只有紅色光的房間內，相同的 crystal 會顯示為黑色，因為它的材質不會反映紅色光源。</span><span class="sxs-lookup"><span data-stu-id="79363-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="79363-123">排放</span><span class="sxs-lookup"><span data-stu-id="79363-123">Emission</span></span>

<span data-ttu-id="79363-124">材質可以用來讓轉譯的物件看似自我 luminous。</span><span class="sxs-lookup"><span data-stu-id="79363-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="79363-125">[**D3DMATERIAL9**](d3dmaterial9.md)結構的放射成員是用來描述已發出光源的色彩和透明度。</span><span class="sxs-lookup"><span data-stu-id="79363-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="79363-126">放射會影響物件的色彩，例如讓深色材質更亮，並呈現部分的發出色彩。</span><span class="sxs-lookup"><span data-stu-id="79363-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="79363-127">您可以使用材質的放射屬性來新增物件發出光線的假像，而不會造成將燈光新增至場景的計算額外負荷。</span><span class="sxs-lookup"><span data-stu-id="79363-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="79363-128">在 blue crystal 的情況下，如果您想要讓 crystal 看起來很亮，而不是在場景中的其他物件上轉換燈光，放射屬性就很有用。</span><span class="sxs-lookup"><span data-stu-id="79363-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="79363-129">請記住，具有放射屬性的材質不會發出可由場景中其他物件反映的燈。</span><span class="sxs-lookup"><span data-stu-id="79363-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="79363-130">若要達到這種反映的光線，您需要在場景內放置額外的燈。</span><span class="sxs-lookup"><span data-stu-id="79363-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="79363-131">反射反映</span><span class="sxs-lookup"><span data-stu-id="79363-131">Specular Reflection</span></span>

<span data-ttu-id="79363-132">反射反映會在物件上建立醒目顯示，讓它們看起來很亮。</span><span class="sxs-lookup"><span data-stu-id="79363-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="79363-133">[**D3DMATERIAL9**](d3dmaterial9.md)結構包含兩個成員，這些成員描述反射反白顯示色彩以及材質的整體反光。</span><span class="sxs-lookup"><span data-stu-id="79363-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="79363-134">您可以藉由將反射成員設定為所需的 RGBA 色彩來建立高光的色彩-最常見的色彩為白色或淺灰色。</span><span class="sxs-lookup"><span data-stu-id="79363-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="79363-135">您在 Power 成員中設定的值會控制反射效果的清晰程度。</span><span class="sxs-lookup"><span data-stu-id="79363-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="79363-136">高光可能會產生顯著的效果。</span><span class="sxs-lookup"><span data-stu-id="79363-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="79363-137">在藍色 crystal 上再次繪圖：較大的功率值會建立更清晰的高光，讓 crystal 看似相當亮。</span><span class="sxs-lookup"><span data-stu-id="79363-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="79363-138">較小的值會增加效果的面積，建立讓 crystal 外觀 frosty 的單調反映。</span><span class="sxs-lookup"><span data-stu-id="79363-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="79363-139">若要將物件設為真正的遮罩，請將 Power 成員設定為零，並將高光中的色彩設定為黑色。</span><span class="sxs-lookup"><span data-stu-id="79363-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="79363-140">試驗不同層級的反映，以針對您的需求產生實際的外觀。</span><span class="sxs-lookup"><span data-stu-id="79363-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="79363-141">下圖顯示兩個相同的模型。</span><span class="sxs-lookup"><span data-stu-id="79363-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="79363-142">左邊的一個會使用10的反射反映乘冪;右邊的模型沒有反射反映。</span><span class="sxs-lookup"><span data-stu-id="79363-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![反射反映模型的圖例](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="79363-144">設定材質屬性</span><span class="sxs-lookup"><span data-stu-id="79363-144">Setting Material Properties</span></span>

<span data-ttu-id="79363-145">Direct3D 轉譯裝置一次只能使用一組材質屬性來呈現。</span><span class="sxs-lookup"><span data-stu-id="79363-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="79363-146">在 c + + 應用程式中，您可以藉由準備 [**D3DMATERIAL9**](d3dmaterial9.md) 結構，然後呼叫 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) 方法，來設定系統所使用的材質屬性。</span><span class="sxs-lookup"><span data-stu-id="79363-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="79363-147">若要準備要使用的 [**D3DMATERIAL9**](d3dmaterial9.md) 結構，請設定結構中的屬性資訊，以在轉譯期間建立所要的效果。</span><span class="sxs-lookup"><span data-stu-id="79363-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="79363-148">下列程式碼範例會為紫色材質設定有清晰白色高光的 **D3DMATERIAL9** 結構。</span><span class="sxs-lookup"><span data-stu-id="79363-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="79363-149">準備 [**D3DMATERIAL9**](d3dmaterial9.md) 結構之後，您可以藉由呼叫轉譯裝置的 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) 方法來套用屬性。</span><span class="sxs-lookup"><span data-stu-id="79363-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="79363-150">這個方法會接受備妥 **D3DMATERIAL9** 結構的位址做為其唯一的參數。</span><span class="sxs-lookup"><span data-stu-id="79363-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="79363-151">您可以視需要使用新的資訊來呼叫 **IDirect3DDevice9：： SetMaterial** ，以更新裝置的材質屬性。</span><span class="sxs-lookup"><span data-stu-id="79363-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="79363-152">下列程式碼範例顯示如何在程式碼中查看。</span><span class="sxs-lookup"><span data-stu-id="79363-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="79363-153">當您建立 Direct3D 裝置時，會自動將目前的材質設定為下表所示的預設值。</span><span class="sxs-lookup"><span data-stu-id="79363-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="79363-154">成員</span><span class="sxs-lookup"><span data-stu-id="79363-154">Member</span></span>   | <span data-ttu-id="79363-155">值</span><span class="sxs-lookup"><span data-stu-id="79363-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="79363-156">擴散</span><span class="sxs-lookup"><span data-stu-id="79363-156">Diffuse</span></span>  | <span data-ttu-id="79363-157"> (R:0、G:0、B:0、A:0) </span><span class="sxs-lookup"><span data-stu-id="79363-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="79363-158">反射</span><span class="sxs-lookup"><span data-stu-id="79363-158">Specular</span></span> | <span data-ttu-id="79363-159"> (R:0、G:0、B:0、A:0) </span><span class="sxs-lookup"><span data-stu-id="79363-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="79363-160">環境</span><span class="sxs-lookup"><span data-stu-id="79363-160">Ambient</span></span>  | <span data-ttu-id="79363-161"> (R:0、G:0、B:0、A:0) </span><span class="sxs-lookup"><span data-stu-id="79363-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="79363-162">放射</span><span class="sxs-lookup"><span data-stu-id="79363-162">Emissive</span></span> | <span data-ttu-id="79363-163"> (R:0、G:0、B:0、A:0) </span><span class="sxs-lookup"><span data-stu-id="79363-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="79363-164">電源</span><span class="sxs-lookup"><span data-stu-id="79363-164">Power</span></span>    | <span data-ttu-id="79363-165"> (0.0) </span><span class="sxs-lookup"><span data-stu-id="79363-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="79363-166">正在抓取材質屬性</span><span class="sxs-lookup"><span data-stu-id="79363-166">Retrieving Material Properties</span></span>

<span data-ttu-id="79363-167">您可以藉由呼叫裝置的 [**IDirect3DDevice9：： GetMaterial**](/windows/desktop/api) 方法，來取出轉譯裝置目前所使用的材質屬性。</span><span class="sxs-lookup"><span data-stu-id="79363-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="79363-168">不同于 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) 方法， **IDirect3DDevice9：： GetMaterial** 不需要準備。</span><span class="sxs-lookup"><span data-stu-id="79363-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="79363-169">**IDirect3DDevice9：： GetMaterial** 方法接受 [**D3DMATERIAL9**](d3dmaterial9.md)結構的位址，並在傳回之前，以描述目前材質屬性的資訊填入提供的結構。</span><span class="sxs-lookup"><span data-stu-id="79363-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="79363-170">如果您的應用程式未指定用於轉譯的材質屬性，系統就會使用預設的材質。</span><span class="sxs-lookup"><span data-stu-id="79363-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="79363-171">預設材質會反映所有的擴散淺白色，例如，沒有環境或反射反映，而且沒有放射色彩。</span><span class="sxs-lookup"><span data-stu-id="79363-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="79363-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="79363-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79363-173">燈光和材質</span><span class="sxs-lookup"><span data-stu-id="79363-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
