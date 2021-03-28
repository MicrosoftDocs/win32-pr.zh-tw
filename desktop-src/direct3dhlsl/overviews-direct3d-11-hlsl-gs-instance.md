---
title: 如何實例幾何著色器
description: 幾何著色器實例允許針對每個基本類型執行相同幾何著色器的多個執行。
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990643"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="8c02b-103">如何：實例幾何著色器</span><span class="sxs-lookup"><span data-stu-id="8c02b-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="8c02b-104">幾何著色器實例允許針對每個基本類型執行相同幾何著色器的多個執行。</span><span class="sxs-lookup"><span data-stu-id="8c02b-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="8c02b-105">若要建立幾何著色器的實例，請將實例屬性加入至主要著色器函式，並識別著色器函式主體中的實例索引參數。</span><span class="sxs-lookup"><span data-stu-id="8c02b-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="8c02b-106">若要建立幾何著色器的實例：</span><span class="sxs-lookup"><span data-stu-id="8c02b-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="8c02b-107">將 [實例屬性](sm5-attributes-instance.md) 加入至 main 函數。</span><span class="sxs-lookup"><span data-stu-id="8c02b-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="8c02b-108">這會定義每個基本 (最多可執行 32) 的實例數目。</span><span class="sxs-lookup"><span data-stu-id="8c02b-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="8c02b-109">將 [ [SV \_ GSInstanceID](sv-gsinstanceid.md) 系統] 值附加至 [函數參數] 清單中的變數，可用來追蹤所執行之實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c02b-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="8c02b-110">編譯和建立著色器，就像任何其他幾何著色器一樣。</span><span class="sxs-lookup"><span data-stu-id="8c02b-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="8c02b-111">其他詳細資料包含：</span><span class="sxs-lookup"><span data-stu-id="8c02b-111">Other details include:</span></span>

-   <span data-ttu-id="8c02b-112">最大實例計數為32。</span><span class="sxs-lookup"><span data-stu-id="8c02b-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="8c02b-113">最大頂點計數是每個實例的最大頂點計數。</span><span class="sxs-lookup"><span data-stu-id="8c02b-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="8c02b-114">每個實例調用 (像任何幾何著色器調用一樣) 增加調用計數，並產生隱含的 RestartStrip () 。</span><span class="sxs-lookup"><span data-stu-id="8c02b-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c02b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c02b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c02b-116">幾何著色器功能</span><span class="sxs-lookup"><span data-stu-id="8c02b-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




