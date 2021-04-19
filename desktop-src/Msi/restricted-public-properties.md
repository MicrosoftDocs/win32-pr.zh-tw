---
description: 在某些情況下，不是系統管理員的使用者只能覆寫受限制 Windows Installer 公用屬性的核准清單。
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: 受限制的公用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980444"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="f0bf4-103">受限制的公用屬性</span><span class="sxs-lookup"><span data-stu-id="f0bf4-103">Restricted Public Properties</span></span>

<span data-ttu-id="f0bf4-104">在受控安裝的情況下，封裝作者可能需要限制哪些 [公用屬性](public-properties.md) 會傳遞至伺服器端，並且可由非系統管理員的使用者進行變更。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="f0bf4-105">當安裝要求安裝程式需要使用較高的許可權時，通常需要一些限制才能維護安全的環境。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="f0bf4-106">如果符合下列所有條件，則不是系統管理員的使用者只能覆寫受限制公用屬性的核准清單：</span><span class="sxs-lookup"><span data-stu-id="f0bf4-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="f0bf4-107">系統是 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="f0bf4-108">使用者不是系統管理員。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="f0bf4-109">正在以較高的許可權安裝應用程式或產品。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="f0bf4-110">如果上述所有條件都成立，則安裝程式會預設為可由任何使用者變更的下列受限制公用屬性清單：</span><span class="sxs-lookup"><span data-stu-id="f0bf4-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="f0bf4-111">**行動**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="f0bf4-112">**AFTERREBOOT**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="f0bf4-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="f0bf4-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="f0bf4-115">**EXECUTEMODE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="f0bf4-116">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="f0bf4-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="f0bf4-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="f0bf4-119">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="f0bf4-120">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="f0bf4-121">**LOGACTION**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="f0bf4-122">**NOCOMPANYNAME**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="f0bf4-123">**NOUSERNAME**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="f0bf4-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="f0bf4-125">**MSIINSTANCEGUID**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="f0bf4-126">**MSINEWINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="f0bf4-127">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="f0bf4-128">**補丁**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="f0bf4-129">**PRIMARYFOLDER**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="f0bf4-130">**PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="f0bf4-131">**重新 啟動**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="f0bf4-132">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="f0bf4-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="f0bf4-134">**恢復**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="f0bf4-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="f0bf4-136">**SHORTFILENAMES**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="f0bf4-137">**變換**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="f0bf4-138">**TRANSFORMSATSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f0bf4-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="f0bf4-139">安裝套件的作者可以使用 [**SecureCustomProperties**](securecustomproperties.md) 屬性，擴充此預設清單以包含其他公用屬性。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="f0bf4-140">設定 [**EnableUserControl**](-enableusercontrol.md) 屬性或 [EnableUserControl](enableusercontrol.md)[系統原則](system-policy.md) 會將清單延伸至所有公用屬性。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="f0bf4-141">然後，所有使用者都可以變更任何公用屬性。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-141">All users can then change any public property.</span></span>

<span data-ttu-id="f0bf4-142">每當非系統管理員使用者傳遞給伺服器的公用屬性清單受到限制時，安裝程式就會設定 [**RestrictedUserControl**](restrictedusercontrol.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f0bf4-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0bf4-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0bf4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0bf4-144">關於屬性</span><span class="sxs-lookup"><span data-stu-id="f0bf4-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



