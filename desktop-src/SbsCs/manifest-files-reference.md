---
description: 並存元件可與下列類型的資訊清單和設定檔搭配使用。 資訊清單和設定為 XML 檔案。
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: "  資訊清單檔案參考"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112704"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="821e1-104">  資訊清單檔案參考</span><span class="sxs-lookup"><span data-stu-id="821e1-104">Manifest Files Reference</span></span>

<span data-ttu-id="821e1-105">並存元件可與下列類型的資訊清單和設定檔搭配使用。</span><span class="sxs-lookup"><span data-stu-id="821e1-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="821e1-106">資訊清單和設定為 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="821e1-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="821e1-107">file:///</span><span class="sxs-lookup"><span data-stu-id="821e1-107">Manifest</span></span>                                                               | <span data-ttu-id="821e1-108">Description</span><span class="sxs-lookup"><span data-stu-id="821e1-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="821e1-109">組件資訊清單</span><span class="sxs-lookup"><span data-stu-id="821e1-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="821e1-110">描述並存元件的名稱、版本、資源和元件相依性。</span><span class="sxs-lookup"><span data-stu-id="821e1-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="821e1-111">應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="821e1-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="821e1-112">描述應用程式在執行時間應系結的共用並存元件名稱和版本，也可能包含應用程式所使用之私用並存元件的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="821e1-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="821e1-113">應用程式組態檔</span><span class="sxs-lookup"><span data-stu-id="821e1-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="821e1-114">使用 [每個應用程式](per-application-configuration.md)設定，重新導向元件相依性的元件版本。</span><span class="sxs-lookup"><span data-stu-id="821e1-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="821e1-115">發行者設定檔</span><span class="sxs-lookup"><span data-stu-id="821e1-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="821e1-116">使用 [發行者](publisher-configuration.md)設定，重新導向每個元件的元件相依性元件版本。</span><span class="sxs-lookup"><span data-stu-id="821e1-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="821e1-117">如需資訊清單檔案架構的清單，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="821e1-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="821e1-118">如需應用程式佈建檔架構的清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="821e1-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="821e1-119">如需發行者設定檔架構的清單，請參閱 [發行者設定檔架構](publisher-configuration-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="821e1-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="821e1-120">其他技術則擴充了 Windows 版本控制和設定資訊清單所使用的格式。</span><span class="sxs-lookup"><span data-stu-id="821e1-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="821e1-121">開發人員應該參考用來取得資訊清單格式相關資訊之技術的相關檔。</span><span class="sxs-lookup"><span data-stu-id="821e1-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="821e1-122">例如：</span><span class="sxs-lookup"><span data-stu-id="821e1-122">For example:</span></span>

-   [<span data-ttu-id="821e1-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="821e1-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="821e1-124">Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="821e1-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="821e1-125">[使用者帳戶控制 (UAC)](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="821e1-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 
