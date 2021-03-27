---
title: 儲存要共用之著色器的變數和類型
description: 類別連結化物件是多個著色器可以共用之變數和類型的命名空間。
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971784"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="f0bbe-103">儲存要共用之著色器的變數和類型</span><span class="sxs-lookup"><span data-stu-id="f0bbe-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="f0bbe-104">類別連結化物件是多個著色器可以共用之變數和類型的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="f0bbe-105">當您在呼叫中傳遞類別連結化物件來建立著色器時，執行時間會收集可在著色器中執行每個介面的變數和類型清單，並在類別連結化物件中儲存這些變數和類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="f0bbe-106">因此，當您呼叫 [**ID3D11ClassLinkage：： GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) 方法從類別連結化物件產生類別實例時，執行時間可以取得對應至每個著色器中所提供之名稱的變數或類型 (如果該名稱對於指定的著色器) 有效，且是以指定的類別連結化物件所建立。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="f0bbe-107">例如，假設您的 **輕** 量類別會實 **色** 介面，而且您會在頂點著色器和圖元著色器中使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="f0bbe-108">當您建立著色器 (例如，藉由呼叫 [**ID3D11Device：： CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)) ，執行時間會判斷在頂點和圖元著色器中都可使用 **light** 類別類型，並將 **燈光** 類別類型加入至類別連結化物件。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="f0bbe-109">然後，您可以在想要的位置上建立 **輕** 量實例、系結這兩個著色器的資源，並在將著色器設定為裝置時，在類別實例陣列中傳遞這個實例 (例如，藉由呼叫 [**>id3d11devicecoNtext：:P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)) 。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="f0bbe-110">執行時間接著會執行下列順序：</span><span class="sxs-lookup"><span data-stu-id="f0bbe-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="f0bbe-111">確認已使用相同的類別連結化物件建立實例。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="f0bbe-112">確認在頂點和圖元著色器中推出 **淺色** 類別類型。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="f0bbe-113">選取正確的函式資料表，這在頂點和圖元著色器中可能會不同。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="f0bbe-114">向下傳送實例提供的位移。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="f0bbe-115">類別連結化物件最終是型別和變數名稱的儲存機制。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="f0bbe-116">每個專案的可用名稱數目上限 (類型和變數) 是64K。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="f0bbe-117">型別和變數名稱越長，儲存體需求就越高，就是每個著色器儲存的介面中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="f0bbe-118">這是因為執行時間必須為每個著色器儲存這些名稱的對應。</span><span class="sxs-lookup"><span data-stu-id="f0bbe-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0bbe-119">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="f0bbe-119">Related Topics</span></span>

[<span data-ttu-id="f0bbe-120">動態連結</span><span class="sxs-lookup"><span data-stu-id="f0bbe-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="f0bbe-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0bbe-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0bbe-122">動態連結</span><span class="sxs-lookup"><span data-stu-id="f0bbe-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 