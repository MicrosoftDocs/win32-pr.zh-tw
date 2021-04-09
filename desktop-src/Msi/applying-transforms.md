---
description: '[轉換] 屬性包含安裝套件的轉換清單。 安裝程式會在每次安裝、公告、隨選安裝或封裝的維護安裝時，套用轉換清單中的所有轉換。'
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: 套用轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848970"
---
# <a name="applying-transforms"></a><span data-ttu-id="25083-104">套用轉換</span><span class="sxs-lookup"><span data-stu-id="25083-104">Applying Transforms</span></span>

<span data-ttu-id="25083-105">[ [**轉換**](transforms.md) ] 屬性包含安裝套件的轉換清單。</span><span class="sxs-lookup"><span data-stu-id="25083-105">The [**TRANSFORMS**](transforms.md) property contains the list of transforms for an installation package.</span></span> <span data-ttu-id="25083-106">安裝程式會在每次安裝、公告、隨選安裝或封裝的維護安裝時，套用轉換清單中的所有轉換。</span><span class="sxs-lookup"><span data-stu-id="25083-106">The installer applies all the transforms in the transforms list at every installation, advertisement, installation-on-demand, or maintenance installation of the package.</span></span>

<span data-ttu-id="25083-107">[**轉換**](transforms.md)屬性是藉由在命令列上指定轉換的清單來設定。不過，使用/jm 或/ju [命令列選項](command-line-options.md)時，必須使用/t 選項指定轉換清單。</span><span class="sxs-lookup"><span data-stu-id="25083-107">The [**TRANSFORMS**](transforms.md) property is set by specifying the list of transforms on the command line; however, when using either the /jm or /ju [command line option](command-line-options.md), the transforms list must be specified using the /t option.</span></span>

<span data-ttu-id="25083-108">請注意，無法在安裝後修改轉換清單，而且只能藉由卸載應用程式來移除。</span><span class="sxs-lookup"><span data-stu-id="25083-108">Note that the transforms list cannot be modified once installed and can only be removed by uninstalling the application.</span></span>

> [!Note]  
> <span data-ttu-id="25083-109">在安裝應用程式或更新時，Windows Installer 套件可以套用255以上的轉換。</span><span class="sxs-lookup"><span data-stu-id="25083-109">A Windows Installer package can apply no more than 255 transforms when installing an application or update.</span></span> <span data-ttu-id="25083-110">當需要許多轉換時，應該將它們合併，且應該消除先前已淘汰的轉換。</span><span class="sxs-lookup"><span data-stu-id="25083-110">When many transforms are necessary, they should be combined and previous obsolete transforms should be eliminated.</span></span>

 

<span data-ttu-id="25083-111">下表提供各種可新增至轉換清單的轉換字串範例。</span><span class="sxs-lookup"><span data-stu-id="25083-111">The following table provides examples of various transforms strings that could be added to the transforms list.</span></span>



| <span data-ttu-id="25083-112">轉換字串</span><span class="sxs-lookup"><span data-stu-id="25083-112">Transforms string</span></span>                                                                                                              | <span data-ttu-id="25083-113">Description</span><span class="sxs-lookup"><span data-stu-id="25083-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25083-114">transform1 .mst;： transform2 .mst;： transform3 .mst</span><span class="sxs-lookup"><span data-stu-id="25083-114">transform1.mst;:transform2.mst;:transform3.mst</span></span>                                                                                 | <span data-ttu-id="25083-115">Transform2 .mst 和 transform3 是 [內嵌的轉換](embedded-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="25083-115">Transform2.mst and transform3.mst are [embedded transforms](embedded-transforms.md).</span></span> <span data-ttu-id="25083-116">transform1 只有在已設定 [**TRANSFORMSSECURE**](transformssecure.md)屬性或 [TRANSFORMSSECURE 原則](transformssecure-policy.md)時，才是 [安全的來源轉換](secure-at-source-transforms.md)，否則 transform1 是不 [安全的轉換](unsecured-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="25083-116">transform1.mst is a [secure-at-source transform](secure-at-source-transforms.md) only if the [**TRANSFORMSSECURE**](transformssecure.md) property or [TransformsSecure policy](transformssecure-policy.md) is set, otherwise transform1 is an [unsecured transform](unsecured-transforms.md).</span></span> |
| <span data-ttu-id="25083-117">\\\\伺服器 \\ 共用 \\ 路徑 \\ transform1 .mst;： transform2 .mst</span><span class="sxs-lookup"><span data-stu-id="25083-117">\\\\server\\share\\path\\transform1.mst;:transform2.mst</span></span>                                                                        | <span data-ttu-id="25083-118">Transform2 是 [內嵌的轉換](embedded-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="25083-118">Transform2.mst is an [embedded transform](embedded-transforms.md).</span></span> <span data-ttu-id="25083-119">transform1 只有在設定 [**TRANSFORMSSECURE**](transformssecure.md)屬性或 [TRANSFORMSSECURE 原則](transformssecure-policy.md)時，才會使用 [安全的完整路徑轉換](secure-full-path-transforms.md)，否則 transform1 是不安全的 [轉換](unsecured-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="25083-119">transform1.mst is a [secure-full-path transform](secure-full-path-transforms.md) only if the [**TRANSFORMSSECURE**](transformssecure.md) property or [TransformsSecure policy](transformssecure-policy.md) is set, otherwise transform1 is an [unsecured transform](unsecured-transforms.md).</span></span>                   |
| <span data-ttu-id="25083-120">@： transform2 .mst; transform1 .mst @transform1.mst ;： transform2 .mst</span><span class="sxs-lookup"><span data-stu-id="25083-120">@:transform2.mst;transform1.mst @transform1.mst;:transform2.mst</span></span><br/>                                                     | <span data-ttu-id="25083-121">Transform2 是內嵌的轉換。</span><span class="sxs-lookup"><span data-stu-id="25083-121">Transform2.mst is an embedded transform.</span></span> <span data-ttu-id="25083-122">transform1 是獨立的 [安全來源轉換](secure-at-source-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="25083-122">transform1.mst is a stand-alone [secure-at-source transforms](secure-at-source-transforms.md).</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="25083-123">\|\\\\伺服器 \\ 共用 \\ 路徑 \\ transform1 .mst;： transform2 .mst \| ： transform2 .mst; \\ \\伺服器 \\ 共用 \\ 路徑 \\ transform1 .mst</span><span class="sxs-lookup"><span data-stu-id="25083-123">\|\\\\server\\share\\path\\transform1.mst;:transform2.mst \|:transform2.mst;\\\\server\\share\\path\\transform1.mst</span></span><br/> | <span data-ttu-id="25083-124">Transform2 是內嵌的轉換。</span><span class="sxs-lookup"><span data-stu-id="25083-124">Transform2.mst is an embedded transform.</span></span> <span data-ttu-id="25083-125">transform1 是獨立的 [安全-完整路徑轉換](secure-full-path-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="25083-125">transform1.mst is a Standalone [secure-full-path transforms](secure-full-path-transforms.md).</span></span>                                                                                                                                                                                                                                                 |



 

 

 




