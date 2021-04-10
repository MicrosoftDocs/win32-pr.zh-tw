---
description: Msizap.exe 是一種命令列公用程式，可移除產品的所有 Windows Installer 資訊，或電腦上安裝的所有產品。 使用 Msizap 之後，安裝程式所安裝的產品可能無法運作。
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026560"
---
# <a name="msizapexe"></a><span data-ttu-id="1916b-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="1916b-104">Msizap.exe</span></span>

<span data-ttu-id="1916b-105">Msizap.exe 是一種命令列公用程式，可移除產品的所有 Windows Installer 資訊，或電腦上安裝的所有產品。</span><span class="sxs-lookup"><span data-stu-id="1916b-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="1916b-106">使用 Msizap 之後，安裝程式所安裝的產品可能無法運作。</span><span class="sxs-lookup"><span data-stu-id="1916b-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="1916b-107">在 Windows 2000 和 Windows XP 上，需要有系統管理許可權才能使用 Msizap.exe。</span><span class="sxs-lookup"><span data-stu-id="1916b-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="1916b-108">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md) ，不應轉散發。</span><span class="sxs-lookup"><span data-stu-id="1916b-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="1916b-109">使用適用于 Windows Vista 或更新版本的 Windows Installer 開發人員 Windows SDK 元件中提供的 Msizap.exe (版本3.1.4000.2726 或更高版本) 。</span><span class="sxs-lookup"><span data-stu-id="1916b-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="1916b-110">較低版本的 Msizap.exe 可以移除已套用至使用者電腦上其他應用程式之所有更新的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1916b-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="1916b-111">如果移除此資訊，可能需要移除並重新安裝這些其他應用程式才能接收其他更新。</span><span class="sxs-lookup"><span data-stu-id="1916b-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1916b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="1916b-112">Syntax</span></span>

<span data-ttu-id="1916b-113">**msizap T** _\[ WA！ \]{產品代碼}_</span><span class="sxs-lookup"><span data-stu-id="1916b-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="1916b-114">**msizap T** _\[ WA！ \] <msi package>_</span><span class="sxs-lookup"><span data-stu-id="1916b-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="1916b-115">**\* \*\*\* msizap \[WA！ \]\*\*\*ALLPRODUCTS**</span><span class="sxs-lookup"><span data-stu-id="1916b-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="1916b-116">**msizap PWSA？！**</span><span class="sxs-lookup"><span data-stu-id="1916b-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="1916b-117">命令列選項</span><span class="sxs-lookup"><span data-stu-id="1916b-117">Command Line Options</span></span>

<span data-ttu-id="1916b-118">Msizap.exe 使用下表所示的不區分大小寫命令列選項。</span><span class="sxs-lookup"><span data-stu-id="1916b-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="1916b-119">選項</span><span class="sxs-lookup"><span data-stu-id="1916b-119">Option</span></span> | <span data-ttu-id="1916b-120">Description</span><span class="sxs-lookup"><span data-stu-id="1916b-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="1916b-121">移除所有 Windows Installer 資料夾和登錄機碼、調整共用的 DLL 計數，並停止 Windows Installer 服務。</span><span class="sxs-lookup"><span data-stu-id="1916b-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="1916b-122">也會移除 In-Progress 金鑰和復原資訊。</span><span class="sxs-lookup"><span data-stu-id="1916b-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="1916b-123">a</span><span class="sxs-lookup"><span data-stu-id="1916b-123">a</span></span>      | <span data-ttu-id="1916b-124">只會針對任何指定的移除，將 Acl 變更為系統管理員的完全控制。</span><span class="sxs-lookup"><span data-stu-id="1916b-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="1916b-125">g</span><span class="sxs-lookup"><span data-stu-id="1916b-125">g</span></span>      | <span data-ttu-id="1916b-126">針對所有使用者，移除任何已孤立的快取 Windows Installer 資料檔案。</span><span class="sxs-lookup"><span data-stu-id="1916b-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="1916b-127">p</span><span class="sxs-lookup"><span data-stu-id="1916b-127">p</span></span>      | <span data-ttu-id="1916b-128">移除 In-Progress 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1916b-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="1916b-129">s</span><span class="sxs-lookup"><span data-stu-id="1916b-129">s</span></span>      | <span data-ttu-id="1916b-130">移除復原資訊。</span><span class="sxs-lookup"><span data-stu-id="1916b-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="1916b-131">t</span><span class="sxs-lookup"><span data-stu-id="1916b-131">t</span></span>      | <span data-ttu-id="1916b-132">移除指定產品代碼的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="1916b-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="1916b-133">使用這個選項時，請將產品代碼放在大括弧中。</span><span class="sxs-lookup"><span data-stu-id="1916b-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="1916b-134">此選項可搭配 .msi 檔案的完整路徑或產品代碼使用。</span><span class="sxs-lookup"><span data-stu-id="1916b-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="1916b-135">w</span><span class="sxs-lookup"><span data-stu-id="1916b-135">w</span></span>      | <span data-ttu-id="1916b-136">移除所有使用者的 Windows Installer 資訊。</span><span class="sxs-lookup"><span data-stu-id="1916b-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="1916b-137">如果未設定此選項，則只會移除目前使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="1916b-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="1916b-138">使用這個選項需要載入使用者的設定檔，才能使用使用者的每個使用者登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="1916b-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="1916b-139">?</span><span class="sxs-lookup"><span data-stu-id="1916b-139">?</span></span>      | <span data-ttu-id="1916b-140">詳細資訊說明。</span><span class="sxs-lookup"><span data-stu-id="1916b-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1916b-141">!</span><span class="sxs-lookup"><span data-stu-id="1916b-141">!</span></span>      | <span data-ttu-id="1916b-142">強制對任何提示輸入「是」回應。</span><span class="sxs-lookup"><span data-stu-id="1916b-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="1916b-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="1916b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1916b-144">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1916b-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



