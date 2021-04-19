---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: 'G (隔離的應用程式和並存元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972396"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="a2759-103">G (隔離的應用程式和並存元件) </span><span class="sxs-lookup"><span data-stu-id="a2759-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="a2759-104">[B C](a-sbscs-gly.md) [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z</span><span class="sxs-lookup"><span data-stu-id="a2759-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a2759-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**全域應用程式設定**</span><span class="sxs-lookup"><span data-stu-id="a2759-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="a2759-106">規格：系統上的所有應用程式都使用相同的並存元件版本。</span><span class="sxs-lookup"><span data-stu-id="a2759-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="a2759-107">全域設定是針對安裝在 Winsxs 資料夾中的全域組件資訊清單檔，以每個元件為基礎來指定。</span><span class="sxs-lookup"><span data-stu-id="a2759-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="a2759-108">當元件開發人員或系統管理員需要將系統上的所有應用程式設定為使用較新的元件版本時，可能會使用全域設定。</span><span class="sxs-lookup"><span data-stu-id="a2759-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="a2759-109">在此情況下，新的元件必須具有回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="a2759-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="a2759-110">針對特定應用程式，每個應用程式的設定會覆寫預設或全域應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="a2759-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="a2759-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**全域組件資訊清單**</span><span class="sxs-lookup"><span data-stu-id="a2759-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="a2759-112">定義並存元件之全域應用程式設定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a2759-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="a2759-113">全域組件資訊清單檔會安裝到 Winsxs 資料夾中的系統元件存放區。</span><span class="sxs-lookup"><span data-stu-id="a2759-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



