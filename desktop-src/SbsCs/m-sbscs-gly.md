---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 726518FB-FCED-433B-BDD1-3B141C17AF32
title: 'M (隔離的應用程式和並存元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420f39a65864659fb48e0492c87070cc97a3c6bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690155"
---
# <a name="m-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="550e8-103">M (隔離的應用程式和並存元件) </span><span class="sxs-lookup"><span data-stu-id="550e8-103">M (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="550e8-104">[B C](a-sbscs-gly.md) [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L M N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z</span><span class="sxs-lookup"><span data-stu-id="550e8-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L M N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="550e8-105"><span id="_win32_manifest_file_gly"></span><span id="_WIN32_MANIFEST_FILE_GLY"></span>**資訊清單檔**</span><span class="sxs-lookup"><span data-stu-id="550e8-105"><span id="_win32_manifest_file_gly"></span><span id="_WIN32_MANIFEST_FILE_GLY"></span>**manifest file**</span></span>
</dt> <dd>

<span data-ttu-id="550e8-106">描述並存元件或隔離應用程式的 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="550e8-106">XML file that describes a side-by-side assembly or an isolated application.</span></span> <span data-ttu-id="550e8-107">資訊清單檔案可能包含傳統儲存在登錄中的系結和啟用中繼資料，例如 COM 類別、介面和型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="550e8-107">A manifest file may contain binding and activation metadata traditionally stored in the registry, such as COM classes, interfaces, and type libraries.</span></span> <span data-ttu-id="550e8-108">每個隔離的應用程式或並存元件都會伴隨資訊清單檔案。</span><span class="sxs-lookup"><span data-stu-id="550e8-108">Every isolated application or side-by-side assembly is accompanied by a manifest file.</span></span> <span data-ttu-id="550e8-109">應用程式資訊清單描述完整或部分隔離的應用程式，而組件資訊清單則描述並存元件。</span><span class="sxs-lookup"><span data-stu-id="550e8-109">An application manifest describes a fully or partially isolated application and an assembly manifest describes a side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="550e8-110"><span id="_win32_metadata_gly"></span><span id="_WIN32_METADATA_GLY"></span>**元**</span><span class="sxs-lookup"><span data-stu-id="550e8-110"><span id="_win32_metadata_gly"></span><span id="_WIN32_METADATA_GLY"></span>**metadata**</span></span>
</dt> <dd>

<span data-ttu-id="550e8-111">儲存在資訊清單檔中的資訊，有關隔離的應用程式或並存元件的系結或啟用。</span><span class="sxs-lookup"><span data-stu-id="550e8-111">Information stored in a manifest file about the binding or activation of an isolated application or side-by-side assembly.</span></span> <span data-ttu-id="550e8-112">例如，以傳統方式儲存在登錄中的 COM 類別、介面和類型程式庫的相關資訊，可能會以中繼資料的形式儲存在資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="550e8-112">For example, information about COM classes, interfaces and type libraries, traditionally stored in the registry may be stored as metadata in a manifest.</span></span> <span data-ttu-id="550e8-113">中繼資料會描述構成元件的專案，以及其對其他並存元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="550e8-113">Metadata describes the items that make up an assembly and its dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="550e8-114">應用程式資訊清單和相依元件中指定的中繼資料，可用來填入啟用內容。</span><span class="sxs-lookup"><span data-stu-id="550e8-114">The metadata specified in the application manifest and dependent assemblies may be used to populate the activation context.</span></span>

</dd> </dl>

 

 



