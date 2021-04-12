---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: 'P (隔離的應用程式和並存元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386074"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="aab4b-103">P (隔離的應用程式和並存元件) </span><span class="sxs-lookup"><span data-stu-id="aab4b-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="aab4b-104">[B C](a-sbscs-gly.md) [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z</span><span class="sxs-lookup"><span data-stu-id="aab4b-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="aab4b-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**每個應用程式設定**</span><span class="sxs-lookup"><span data-stu-id="aab4b-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="aab4b-106">可以覆寫特定元件的全域應用程式設定的設定。</span><span class="sxs-lookup"><span data-stu-id="aab4b-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="aab4b-107">每個應用程式的設定是由安裝在與可執行檔相同資料夾中的應用程式設定資訊清單檔所指定。</span><span class="sxs-lookup"><span data-stu-id="aab4b-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="aab4b-108">資訊清單檔案會描述應用程式所要使用之並存元件的版本或版本範圍。</span><span class="sxs-lookup"><span data-stu-id="aab4b-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="aab4b-109">當新版本的元件與應用程式不相容時，可能會使用每個應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="aab4b-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="aab4b-110">在此情況下，可以針對特定並存元件覆寫應用程式的預設或全域設定。</span><span class="sxs-lookup"><span data-stu-id="aab4b-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="aab4b-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**私用並存元件**</span><span class="sxs-lookup"><span data-stu-id="aab4b-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="aab4b-112">私用並存元件只有指定的應用程式可以看見。</span><span class="sxs-lookup"><span data-stu-id="aab4b-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="aab4b-113">它會在本機安裝至隔離的應用程式，而元件的程式碼則會成為應用程式內容的私用。</span><span class="sxs-lookup"><span data-stu-id="aab4b-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="aab4b-114">私用並存元件的相依性會在應用程式資訊清單檔中描述。</span><span class="sxs-lookup"><span data-stu-id="aab4b-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="aab4b-115">私用並存元件可以用來抵消元件共用的負面影響，例如 DLL 衝突，以及簡化應用程式部署。</span><span class="sxs-lookup"><span data-stu-id="aab4b-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="aab4b-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**公開金鑰 token**</span><span class="sxs-lookup"><span data-stu-id="aab4b-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="aab4b-117">16字元的十六進位字串，表示用來簽署元件之公開金鑰的 SHA-1 雜湊最後8個位元組。</span><span class="sxs-lookup"><span data-stu-id="aab4b-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="aab4b-118">用來簽署目錄的公開金鑰必須是2048位或更高的版本。</span><span class="sxs-lookup"><span data-stu-id="aab4b-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="aab4b-119">所有共用並存元件的必要項。</span><span class="sxs-lookup"><span data-stu-id="aab4b-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 



