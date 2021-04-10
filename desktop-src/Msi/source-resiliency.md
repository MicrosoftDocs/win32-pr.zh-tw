---
description: 依賴網路資源進行隨選安裝的應用程式，可能會因為來源位置因任何原因而變更或損毀，而受到來源失敗的影響。
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: 來源復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936644"
---
# <a name="source-resiliency"></a><span data-ttu-id="6fe72-103">來源復原</span><span class="sxs-lookup"><span data-stu-id="6fe72-103">Source Resiliency</span></span>

<span data-ttu-id="6fe72-104">依賴網路資源進行 [隨選安裝](installation-on-demand.md) 的應用程式，可能會因為來源位置因任何原因而變更或損毀，而受到來源失敗的影響。</span><span class="sxs-lookup"><span data-stu-id="6fe72-104">Applications that rely on network resources for [installation-on-demand](installation-on-demand.md) are susceptible to source failures if the source location should change for any reason or become damaged.</span></span> <span data-ttu-id="6fe72-105">Windows Installer 會使用來源清單，為隨選安裝的功能提供來源復原功能。</span><span class="sxs-lookup"><span data-stu-id="6fe72-105">The Windows Installer provides source resiliency for features that are installed on-demand by using a source list.</span></span> <span data-ttu-id="6fe72-106">來源清單包含安裝套件安裝程式所搜尋的位置。</span><span class="sxs-lookup"><span data-stu-id="6fe72-106">The source list contains the locations searched by the installer for installation packages.</span></span> <span data-ttu-id="6fe72-107">這份清單中的專案可以是網路位置、統一資源定位器 (Url) 或 compact 光碟。</span><span class="sxs-lookup"><span data-stu-id="6fe72-107">The entries in this list can be network locations, Uniform Resource Locators (URLs), or compact discs.</span></span> <span data-ttu-id="6fe72-108">如果其中一項來源失敗，安裝程式可以快速且順暢地嘗試下一個。</span><span class="sxs-lookup"><span data-stu-id="6fe72-108">If one of these sources fails, the installer can quickly and seamlessly try the next.</span></span>

<span data-ttu-id="6fe72-109">應用程式開發人員不需要將任何特殊資訊納入安裝程式套件，以確保來源復原。</span><span class="sxs-lookup"><span data-stu-id="6fe72-109">The application developer does not need to incorporate any special information into the installer package to ensure source resiliency.</span></span> <span data-ttu-id="6fe72-110">一旦安裝應用程式，安裝程式就會將最後一個成功使用的來源新增為來源清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="6fe72-110">Once the application is installed, the installer has the behavior of adding the last successfully used source as an entry in the source list.</span></span> <span data-ttu-id="6fe72-111">根據預設，此來源是安裝程式套件最初安裝所在的位置，與 [**SourceDir**](sourcedir.md) 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="6fe72-111">By default, this source is the location from which the installer package is initially installed, and is the same as the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="6fe72-112">系統管理員可以藉由套用 [轉換](merges-and-transforms.md)或從命令列或在 [屬性工作表](property-table.md)中變更 [**SOURCELIST**](sourcelist.md)屬性，來變更來源清單。</span><span class="sxs-lookup"><span data-stu-id="6fe72-112">A system administrator can change the source list by applying a [transform](merges-and-transforms.md) or by changing the [**SOURCELIST**](sourcelist.md) property from the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="6fe72-113">安裝程式會藉由檢查來源清單中最近使用的來源位置，開始搜尋來源。</span><span class="sxs-lookup"><span data-stu-id="6fe72-113">The installer begins searching for a source by checking the most recently used source location in the source list.</span></span> <span data-ttu-id="6fe72-114">如果此搜尋失敗，安裝程式會搜尋網路來源清單、媒體來源和最後的 URL 來源。</span><span class="sxs-lookup"><span data-stu-id="6fe72-114">If this search fails, the installer searches the list of network sources, then media sources, and finally URL sources.</span></span> <span data-ttu-id="6fe72-115">系統管理員可以使用 [SearchOrder](searchorder.md) 系統原則來變更此搜尋順序。</span><span class="sxs-lookup"><span data-stu-id="6fe72-115">System administrators can change this search order using the [SearchOrder](searchorder.md) system policy.</span></span> <span data-ttu-id="6fe72-116">如果這些搜尋失敗，安裝程式可能會顯示 [流覽對話方塊](browse-dialog.md) ，讓使用者可以手動搜尋來源。</span><span class="sxs-lookup"><span data-stu-id="6fe72-116">If these searches fail, the installer may present a [Browse Dialog](browse-dialog.md) so that the user can search for the source manually.</span></span> <span data-ttu-id="6fe72-117">如果使用者介面層級設定為 [無]，則無法顯示 [流覽] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6fe72-117">The browse dialog box cannot be displayed if the user interface level is set to None.</span></span> <span data-ttu-id="6fe72-118">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="6fe72-118">For details, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="6fe72-119">通常，如果目前的使用者是系統管理員，或如果安裝不需要較高的許可權，安裝程式應該只顯示 [流覽] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6fe72-119">Commonly, the installer should only display a browse dialog box if the current user is an administrator or if the installation does not require elevated privileges.</span></span> <span data-ttu-id="6fe72-120">系統管理員可以控制具有 [DisableBrowse](disablebrowse.md) 和 [AllowLockDownBrowse](allowlockdownbrowse.md) 原則的使用者對 [流覽] 對話方塊的顯示。</span><span class="sxs-lookup"><span data-stu-id="6fe72-120">An administrator can control the display of the browse dialog box to users with the [DisableBrowse](disablebrowse.md) and [AllowLockDownBrowse](allowlockdownbrowse.md) policies.</span></span> <span data-ttu-id="6fe72-121">系統管理員也會控制使用者是否可以使用 [DisableMedia](disablemedia.md) 和 [AllowLockDownMedia](allowlockdownmedia.md) 原則，從位於媒體的來源安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="6fe72-121">An administrator also controls whether users can install applications from sources located on media by using the [DisableMedia](disablemedia.md) and [AllowLockDownMedia](allowlockdownmedia.md) policies.</span></span> <span data-ttu-id="6fe72-122">使用這些原則取決於 Windows Installer 版本。</span><span class="sxs-lookup"><span data-stu-id="6fe72-122">The use of these policies depends on the Windows Installer version.</span></span> <span data-ttu-id="6fe72-123">如需詳細資訊，請參閱下列內容：</span><span class="sxs-lookup"><span data-stu-id="6fe72-123">For details, see the following:</span></span>

-   [<span data-ttu-id="6fe72-124">來源復原原則</span><span class="sxs-lookup"><span data-stu-id="6fe72-124">Source Resiliency Policy</span></span>](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



