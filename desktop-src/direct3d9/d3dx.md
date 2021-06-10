---
description: D3DX 是一種專為在 Direct3D 之上提供其他圖形功能而設計的工具程式庫。 D3DX 是以動態連結程式庫的形式提供， (DLL) 。
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: 'D3DX (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910246"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="7954b-104">D3DX (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="7954b-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="7954b-105">D3DX 程式庫已被取代。</span><span class="sxs-lookup"><span data-stu-id="7954b-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="7954b-106">如果無法選擇升級至較新版本的 Direct3D 和相關聯的公用程式程式碼，您可以使用 [DXSDK D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件，而不是依賴舊版 DirectX SDK 或 DirectSetup。</span><span class="sxs-lookup"><span data-stu-id="7954b-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="7954b-107">D3DX 是一種專為在 Direct3D 之上提供其他圖形功能而設計的工具程式庫。</span><span class="sxs-lookup"><span data-stu-id="7954b-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="7954b-108">D3DX 是以動態連結程式庫的形式提供， (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="7954b-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="7954b-109">這一版的 DirectX SDK 只提供一個版本的 D3DX。</span><span class="sxs-lookup"><span data-stu-id="7954b-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="7954b-110">零售 D3DX DLL 包含在 SDK 所提供的可轉散發套件中，並會在 **使用 DirectSetup 安裝 DirectX** 的過程中自動安裝。</span><span class="sxs-lookup"><span data-stu-id="7954b-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="7954b-111">此版本中包含的 D3DX 程式庫相依于此 SDK 隨附的 Direct3D 執行時間。</span><span class="sxs-lookup"><span data-stu-id="7954b-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="7954b-112">在此版本中連結至 D3DX 版本的應用程式，也必須從這個 SDK 轉散發執行時間。</span><span class="sxs-lookup"><span data-stu-id="7954b-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="7954b-113">多個版本的 D3DX 可同時在單一系統上獨立放置。</span><span class="sxs-lookup"><span data-stu-id="7954b-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="7954b-114">藉由將應用程式以靜態方式連結至 D3dx9，應用程式會在執行時間動態連結至對應的零售 D3DX DLL。</span><span class="sxs-lookup"><span data-stu-id="7954b-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="7954b-115">此 DLL 對應于 D3DX 標頭，此應用程式會針對在 \_ \_) D3dx9core 中以 D3DX SDK 版本常數命名的 (進行編譯。</span><span class="sxs-lookup"><span data-stu-id="7954b-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="7954b-116">當新版本的 D3DX 在未來的 DirectX SDK 版本中寄出時，連結至舊版 D3DX 程式庫的應用程式仍不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="7954b-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="7954b-117">D3DX 程式庫會解決這些一般功能區域：</span><span class="sxs-lookup"><span data-stu-id="7954b-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="7954b-118">D3DX 中的線條繪圖支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="7954b-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="7954b-119">D3DX 中的網格支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="7954b-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="7954b-120">D3DX (Direct3D 9) 中的數學函數支援 </span><span class="sxs-lookup"><span data-stu-id="7954b-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="7954b-121">D3DX 中的材質支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="7954b-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="7954b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="7954b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7954b-123">快速入門</span><span class="sxs-lookup"><span data-stu-id="7954b-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



