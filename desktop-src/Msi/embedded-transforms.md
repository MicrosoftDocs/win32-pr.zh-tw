---
description: 內嵌的轉換會儲存在封裝的 .msi 檔案中。 這可保證使用者在安裝套件可用時，一律可使用轉換。 或者，您可以將轉換提供給使用者作為獨立的 .mst 檔案。
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: 內嵌轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026878"
---
# <a name="embedded-transforms"></a><span data-ttu-id="b4547-105">內嵌轉換</span><span class="sxs-lookup"><span data-stu-id="b4547-105">Embedded Transforms</span></span>

<span data-ttu-id="b4547-106">內嵌的轉換會儲存在封裝的 .msi 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b4547-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="b4547-107">這可保證使用者在安裝套件可用時，一律可使用轉換。</span><span class="sxs-lookup"><span data-stu-id="b4547-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="b4547-108">或者，您可以將轉換提供給使用者作為獨立的 .mst 檔案。</span><span class="sxs-lookup"><span data-stu-id="b4547-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="b4547-109">若要將內嵌轉換新增至轉換清單中，請在檔案名中加入冒號 (： ) 前置詞。</span><span class="sxs-lookup"><span data-stu-id="b4547-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="b4547-110">因為安裝程式一律會從 .msi 檔案中的儲存體取得轉換，所以不會在使用者的電腦上快取內嵌的轉換。</span><span class="sxs-lookup"><span data-stu-id="b4547-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="b4547-111">內嵌的轉換可搭配 [安全的轉換](secured-transforms.md) 或不 [安全的轉換](unsecured-transforms.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="b4547-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="b4547-112">如需詳細資訊，請參閱套用 [轉換](applying-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="b4547-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



