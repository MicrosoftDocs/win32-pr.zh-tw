---
description: Windows Installer 可以執行應用程式或產品的系統管理安裝，以供工作組使用。
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: 系統管理安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3958bdc81ee43cd1a36e0d464f3e77032b4c2d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026646"
---
# <a name="administrative-installation"></a><span data-ttu-id="c9616-103">系統管理安裝</span><span class="sxs-lookup"><span data-stu-id="c9616-103">Administrative Installation</span></span>

<span data-ttu-id="c9616-104">Windows Installer 可以執行應用程式或產品的系統管理安裝，以供工作組使用。</span><span class="sxs-lookup"><span data-stu-id="c9616-104">The Windows Installer can perform an administrative installation of an application or product to a network for use by a workgroup.</span></span> <span data-ttu-id="c9616-105">系統管理安裝會將應用程式的來源映射安裝到網路上，其類似于 CD-ROM 上的來源映射。</span><span class="sxs-lookup"><span data-stu-id="c9616-105">An administrative installation installs a source image of the application onto the network that is similar to a source image on a CD-ROM.</span></span> <span data-ttu-id="c9616-106">工作組中具有此系統管理映射存取權的使用者，可以從這個來源安裝產品。</span><span class="sxs-lookup"><span data-stu-id="c9616-106">Users in a workgroup who have access to this administrative image can then install the product from this source.</span></span> <span data-ttu-id="c9616-107">使用者必須先從網路安裝產品，才能執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="c9616-107">A user must first install the product from the network to run the application.</span></span> <span data-ttu-id="c9616-108">使用者可以選擇在安裝時從來源執行，而且安裝程式會直接從網路使用大部分產品的檔案。</span><span class="sxs-lookup"><span data-stu-id="c9616-108">The user can choose to run-from-source when he installs and the installer uses most of the product's file directly from the network.</span></span>

<span data-ttu-id="c9616-109">系統管理員可以使用/a [命令列選項](command-line-options.md)，從命令列執行系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="c9616-109">Administrators can run an administrative installation from the command line by using the /a [command line option](command-line-options.md).</span></span>

<span data-ttu-id="c9616-110">系統 [管理員動作](admin-action.md) 是用來起始系統管理安裝的最上層動作。</span><span class="sxs-lookup"><span data-stu-id="c9616-110">The [ADMIN action](admin-action.md) is the top-level action used to initiate an administrative installation.</span></span> <span data-ttu-id="c9616-111">執行此動作時，安裝程式會呼叫 [AdminExecuteSequence](adminexecutesequence-table.md) 和 [AdminUISequence](adminuisequence-table.md) 資料表中的動作，以執行系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="c9616-111">When this action is executed the installer calls the actions in the [AdminExecuteSequence](adminexecutesequence-table.md) and [AdminUISequence](adminuisequence-table.md) tables to perform the administrative installation.</span></span>

<span data-ttu-id="c9616-112">[**AdminProperties**](adminproperties.md)屬性是在系統管理安裝時所設定的屬性清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c9616-112">The [**AdminProperties**](adminproperties.md) property is a semicolon delimited list of properties that are set at the time of an administration installation.</span></span> <span data-ttu-id="c9616-113">安裝程式會在應用程式的後續管理安裝期間，從系統管理映射使用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c9616-113">The installer uses these properties during a post administration installation of the application from the administrative image.</span></span>

<span data-ttu-id="c9616-114">沒有連續存取網路的使用者，可能會從系統管理映射安裝應用程式，然後有時必須依賴媒體（如 CD-ROM 磁片）作為其備份來源。</span><span class="sxs-lookup"><span data-stu-id="c9616-114">Users who do not have continuous access to the network may install an application from an administrative image and then at times have to rely on media, such as CD-ROM disks, as their backup source.</span></span> <span data-ttu-id="c9616-115">在這些情況下，系統管理影像和媒體上的檔案名長度必須相符。</span><span class="sxs-lookup"><span data-stu-id="c9616-115">In these cases the length of the file names in the administrative image and on the media must match.</span></span> <span data-ttu-id="c9616-116">兩者都必須使用長檔名，或兩者都必須使用簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c9616-116">Both must use long file names or both must use short file names.</span></span> <span data-ttu-id="c9616-117">例如，只支援簡短檔案名的 CD-ROM 可以提供原始媒體來安裝系統管理映射和備份來源。</span><span class="sxs-lookup"><span data-stu-id="c9616-117">For example, a CD-ROM that only supports short file names could provide both the original media for installing the administrative image and a backup source.</span></span>

<span data-ttu-id="c9616-118">如果在系統管理安裝期間設定了 [**SHORTFILENAMES**](shortfilenames.md) 屬性，則使用者可能需要再次設定此屬性，然後將修補程式套用至系統管理映射。</span><span class="sxs-lookup"><span data-stu-id="c9616-118">If the [**SHORTFILENAMES**](shortfilenames.md) property is set during an administrative installation, this property may need to be set again by a user subsequently applying a patch to the administrative image.</span></span> <span data-ttu-id="c9616-119">使用 Windows Installer 套用修補程式時，如果系統管理映射使用簡短的檔案名，安裝程式會自動設定 **SHORTFILENAMES** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c9616-119">When using Windows Installer to apply the patch, the installer automatically sets the **SHORTFILENAMES** property if the administrative image uses short file names.</span></span>

<span data-ttu-id="c9616-120">如果系統管理員使用具有 [ [**字數統計摘要**](word-count-summary.md) ] 屬性2或3的封裝來執行系統管理安裝，系統管理映射的使用者將無法從原始媒體來源自動重新安裝。</span><span class="sxs-lookup"><span data-stu-id="c9616-120">If an administrator uses a package having a [**Word Count Summary**](word-count-summary.md) property of 2 or 3 to perform an administrative installation, users of the administrative image cannot automatically reinstall from the original media source.</span></span> <span data-ttu-id="c9616-121">如果系統管理映射無法使用，已從系統管理映射安裝的使用者將無法還原到原始媒體。</span><span class="sxs-lookup"><span data-stu-id="c9616-121">If the administrative image becomes unavailable, users who have installed from the administrative image are prevented from reverting to the original media.</span></span>

<span data-ttu-id="c9616-122">在系統管理映射建立期間， [*轉換*](t-gly.md) 的應用程式沒有任何有效的效果。</span><span class="sxs-lookup"><span data-stu-id="c9616-122">The application of [*transforms*](t-gly.md) during the creation of an administrative image has no valid effect.</span></span> <span data-ttu-id="c9616-123">若要將自訂版本的產品提供給工作群組，請從系統管理映射在產品安裝期間套用轉換。</span><span class="sxs-lookup"><span data-stu-id="c9616-123">To make a customized version of a product available to a work group, apply the transform during the installation of the product from the administrative image.</span></span>

<span data-ttu-id="c9616-124">在系統管理安裝期間，安裝程式會針對產品中的所有功能建立來源映射，但 [功能資料表](feature-table.md)的 [層級] 資料行中有0的功能除外。</span><span class="sxs-lookup"><span data-stu-id="c9616-124">During an administrative installation, the installer creates a source image for all features in the product except those feature with 0 in the Level column of the [Feature table](feature-table.md).</span></span>

 

 



