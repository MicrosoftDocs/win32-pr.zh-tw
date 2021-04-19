---
description: 安裝到全域組件快取的 Common language runtime 元件，在所有出現的元件中都必須有相同的檔案。
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Common Language Runtime 元件的重新安裝模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974665"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="da874-103">Common Language Runtime 元件的重新安裝模式</span><span class="sxs-lookup"><span data-stu-id="da874-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="da874-104">安裝到全域組件快取的 Common language runtime 元件，在所有出現的元件中都必須有相同的檔案。</span><span class="sxs-lookup"><span data-stu-id="da874-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="da874-105">這表示 [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) 和 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 所使用的重新安裝模式必須對一般元件和 common language runtime 元件具有不同的意義。</span><span class="sxs-lookup"><span data-stu-id="da874-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="da874-106">下列重新安裝模式的定義適用于 common language runtime 元件。</span><span class="sxs-lookup"><span data-stu-id="da874-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="da874-107">重新安裝模式</span><span class="sxs-lookup"><span data-stu-id="da874-107">Reinstall mode</span></span>                  | <span data-ttu-id="da874-108">Microsoft .NET 元件的意義</span><span class="sxs-lookup"><span data-stu-id="da874-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da874-109">REINSTALLMODE \_ FILEMISSING</span><span class="sxs-lookup"><span data-stu-id="da874-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="da874-110">如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。</span><span class="sxs-lookup"><span data-stu-id="da874-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="da874-111">REINSTALLMODE \_ FILEOLDERVERSION</span><span class="sxs-lookup"><span data-stu-id="da874-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="da874-112">如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。</span><span class="sxs-lookup"><span data-stu-id="da874-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="da874-113">REINSTALLMODE \_ FILEEQUALVERSION</span><span class="sxs-lookup"><span data-stu-id="da874-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="da874-114">如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。</span><span class="sxs-lookup"><span data-stu-id="da874-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="da874-115">REINSTALLMODE \_ FILEEXACT</span><span class="sxs-lookup"><span data-stu-id="da874-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="da874-116">如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。</span><span class="sxs-lookup"><span data-stu-id="da874-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="da874-117">REINSTALLMODE \_ FILEVERIFY</span><span class="sxs-lookup"><span data-stu-id="da874-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="da874-118">如果 common language runtime 元件遺失或現有元件不完整或已損毀，請安裝或重新安裝。</span><span class="sxs-lookup"><span data-stu-id="da874-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="da874-119">REINSTALLMODE \_ FILEREPLACE</span><span class="sxs-lookup"><span data-stu-id="da874-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="da874-120">一律安裝或重新安裝 common language runtime 元件。</span><span class="sxs-lookup"><span data-stu-id="da874-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



