---
description: D3DX 是一種專為在 Direct3D 之上提供其他圖形功能而設計的工具程式庫。 D3DX 是以動態連結程式庫的形式提供， (DLL) 。
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: 'D3DX (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317860"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="1c320-104">D3DX (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1c320-104">D3DX (Direct3D 9)</span></span>

<span data-ttu-id="1c320-105">D3DX 是一種專為在 Direct3D 之上提供其他圖形功能而設計的工具程式庫。</span><span class="sxs-lookup"><span data-stu-id="1c320-105">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="1c320-106">D3DX 是以動態連結程式庫的形式提供， (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="1c320-106">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="1c320-107">這一版的 DirectX SDK 只提供一個版本的 D3DX。</span><span class="sxs-lookup"><span data-stu-id="1c320-107">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="1c320-108">零售 D3DX DLL 包含在 SDK 所提供的可轉散發套件中，並會在 [使用 DirectSetup 安裝 DirectX](https://msdn.microsoft.com/library/ee418267(VS.85).aspx)的過程中自動安裝。</span><span class="sxs-lookup"><span data-stu-id="1c320-108">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span></span> <span data-ttu-id="1c320-109">此版本中包含的 D3DX 程式庫相依于此 SDK 隨附的 Direct3D 執行時間。</span><span class="sxs-lookup"><span data-stu-id="1c320-109">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="1c320-110">在此版本中連結至 D3DX 版本的應用程式，也必須從這個 SDK 轉散發執行時間。</span><span class="sxs-lookup"><span data-stu-id="1c320-110">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="1c320-111">多個版本的 D3DX 可同時在單一系統上獨立放置。</span><span class="sxs-lookup"><span data-stu-id="1c320-111">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="1c320-112">藉由將應用程式以靜態方式連結至 D3dx9，應用程式會在執行時間動態連結至對應的零售 D3DX DLL。</span><span class="sxs-lookup"><span data-stu-id="1c320-112">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="1c320-113">此 DLL 對應于 D3DX 標頭，此應用程式會針對在 \_ \_) D3dx9core 中以 D3DX SDK 版本常數命名的 (進行編譯。</span><span class="sxs-lookup"><span data-stu-id="1c320-113">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="1c320-114">當新版本的 D3DX 在未來的 DirectX SDK 版本中寄出時，連結至舊版 D3DX 程式庫的應用程式仍不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="1c320-114">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="1c320-115">D3DX 程式庫會解決這些一般功能區域：</span><span class="sxs-lookup"><span data-stu-id="1c320-115">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="1c320-116">D3DX 中的線條繪圖支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1c320-116">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="1c320-117">D3DX 中的網格支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1c320-117">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="1c320-118">D3DX (Direct3D 9) 中的數學函數支援 </span><span class="sxs-lookup"><span data-stu-id="1c320-118">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="1c320-119">D3DX 中的材質支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1c320-119">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="1c320-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c320-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c320-121">快速入門</span><span class="sxs-lookup"><span data-stu-id="1c320-121">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



