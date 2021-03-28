---
title: 磚集區建立參數
description: 使用本節中的參數，透過 ID3D11Device CreateBuffer API 定義磚集區。
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020969"
---
# <a name="tile-pool-creation-parameters"></a><span data-ttu-id="12752-103">磚集區建立參數</span><span class="sxs-lookup"><span data-stu-id="12752-103">Tile pool creation parameters</span></span>

<span data-ttu-id="12752-104">使用本節中的參數透過 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API 定義磚集區。</span><span class="sxs-lookup"><span data-stu-id="12752-104">Use the parameters in this section to define tile pools via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API.</span></span>

<dl> <dt>

<span data-ttu-id="12752-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**大小**</span><span class="sxs-lookup"><span data-stu-id="12752-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="12752-106">配置大小需為 64 KB 的倍數</span><span class="sxs-lookup"><span data-stu-id="12752-106">Allocation size, as a multiple of 64KB.</span></span> <span data-ttu-id="12752-107">0有效，因為您稍後可以使用 [**ID3D11DeviceCoNtext2：： ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) 作業。</span><span class="sxs-lookup"><span data-stu-id="12752-107">0 is valid because you can later use a [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation.</span></span>

</dd> <dt>

<span data-ttu-id="12752-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**支援的資源其他旗標**</span><span class="sxs-lookup"><span data-stu-id="12752-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="12752-109">D3D11 \_ 資源 \_ 其他 \_ 磚 \_ 集區 (將資源識別為磚集區) 、D3D11 \_ 資源 \_ 其他 \_ 共用、 \_ 共用 \_ KEYEDMUTEX 或 \_ 共用 \_ NTHANDLE。</span><span class="sxs-lookup"><span data-stu-id="12752-109">D3D11\_RESOURCE\_MISC\_TILE\_POOL (identifies the resource as a tile pool), D3D11\_RESOURCE\_MISC\_SHARED, \_SHARED\_KEYEDMUTEX, or \_SHARED\_NTHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="12752-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**支援的資源使用方式**</span><span class="sxs-lookup"><span data-stu-id="12752-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="12752-111">D3D11 \_ 使用 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="12752-111">D3D11\_USAGE\_DEFAULT only.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="12752-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="12752-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12752-113">建立磚資源</span><span class="sxs-lookup"><span data-stu-id="12752-113">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




