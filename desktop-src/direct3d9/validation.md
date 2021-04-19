---
description: 在效果編譯期間會執行驗證。 若要驗證目前的技巧，請指定 Null 做為要驗證的技術控點。
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: " (Direct3D 9) 驗證"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972106"
---
# <a name="validation-direct3d-9"></a><span data-ttu-id="957a1-104"> (Direct3D 9) 驗證</span><span class="sxs-lookup"><span data-stu-id="957a1-104">Validation (Direct3D 9)</span></span>

<span data-ttu-id="957a1-105">在效果編譯期間會執行驗證。</span><span class="sxs-lookup"><span data-stu-id="957a1-105">Validation is performed during the effect compile.</span></span> <span data-ttu-id="957a1-106">若要驗證目前的技巧，請指定 **Null** 做為要驗證的技術控點。</span><span class="sxs-lookup"><span data-stu-id="957a1-106">To validate the current technique, specify **NULL** as the technique handle to be validated.</span></span>

<span data-ttu-id="957a1-107">下列任何一項的驗證將會失敗：</span><span class="sxs-lookup"><span data-stu-id="957a1-107">Validation will fail for any of the following:</span></span>

-   <span data-ttu-id="957a1-108">如果指定的技術控制碼不存在，則為。</span><span class="sxs-lookup"><span data-stu-id="957a1-108">If the specified technique handle does not exist.</span></span>
-   <span data-ttu-id="957a1-109">如果任何一項技術階段中的任何狀態應用程式都失敗。</span><span class="sxs-lookup"><span data-stu-id="957a1-109">If the application of any state in any pass of the technique fails.</span></span>
-   <span data-ttu-id="957a1-110">如果裝置驗證在應用程式的任何階段中的所有狀態都未通過之後便失敗。</span><span class="sxs-lookup"><span data-stu-id="957a1-110">If device validation fails after the application of all the states in any pass of the technique.</span></span>
-   <span data-ttu-id="957a1-111">如果無效或 VERTEXSHADER 效果狀態是在任何一次的技巧中指派了不正確著色器。</span><span class="sxs-lookup"><span data-stu-id="957a1-111">If the PIXELSHADER or VERTEXSHADER effect states are assigned invalid shaders in any pass of the technique.</span></span>
-   <span data-ttu-id="957a1-112">如果裝置 caps 不支援 cube 對應，且材質效果狀態是在任何一次的技巧中指派為 textureCUBE 類型的值。</span><span class="sxs-lookup"><span data-stu-id="957a1-112">If the device caps do not support cube mapping, and a TEXTURE effect state is assigned a value of type textureCUBE in any pass of the technique.</span></span>
-   <span data-ttu-id="957a1-113">如果裝置 caps 不支援磁片區對應，且材質效果狀態是在任何一次的技巧中指派為 texture3D 類型的值。</span><span class="sxs-lookup"><span data-stu-id="957a1-113">If the device caps do not support volume mapping and a TEXTURE effect state is assigned a value of type texture3D in any pass of the technique.</span></span>

<span data-ttu-id="957a1-114">如需詳細資訊，請參閱 [效果狀態 (Direct3D 9) ](effect-states.md)。</span><span class="sxs-lookup"><span data-stu-id="957a1-114">For more information, see [Effect States (Direct3D 9)](effect-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="957a1-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="957a1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="957a1-116">效果格式</span><span class="sxs-lookup"><span data-stu-id="957a1-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



