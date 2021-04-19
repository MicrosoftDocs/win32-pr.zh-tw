---
description: MsiConfigureServices 動作會設定系統的服務。 此動作會查詢 MsiServiceConfig 和 MsiServiceConfigFailureActions 資料表。
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: MsiConfigureServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980100"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="d8d3a-104">MsiConfigureServices 動作</span><span class="sxs-lookup"><span data-stu-id="d8d3a-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="d8d3a-105">MsiConfigureServices 動作會設定系統的服務。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="d8d3a-106">此動作會查詢 [MsiServiceConfig](msiserviceconfig-table.md) 和 [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="d8d3a-107">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d8d3a-108">從 Windows Installer 5.0 開始，可以使用此動作。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d8d3a-109">Windows 服務能讓您自動執行預先定義的動作，以回應服務中的失敗。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="d8d3a-110">為了支援在服務失敗時以程式設計方式設定這些復原 **動作** ， [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) 已新增至 msi 5.0 版中的 msi。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="d8d3a-111">不過，這項功能不會如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="d8d3a-112">若要解決這個問題，應用程式開發人員應該使用 MSI 中的 **自訂動作** 功能來執行 **sc.exe** 並適當地設定 **修復選項** 。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="d8d3a-113">順序限制</span><span class="sxs-lookup"><span data-stu-id="d8d3a-113">Sequence Restrictions</span></span>

<span data-ttu-id="d8d3a-114">此標準動作必須以下列順序使用。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="d8d3a-115">StopServices</span><span class="sxs-lookup"><span data-stu-id="d8d3a-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="d8d3a-116">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="d8d3a-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="d8d3a-117">下列任何一個動作： [InstallFiles](installfiles-action.md)、 [RemoveFiles](removefiles-action.md)、 [DuplicateFiles](duplicatefiles-action.md)、 [MoveFiles](movefiles-action.md)、 [PatchFiles](patchfiles-action.md)和 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="d8d3a-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="d8d3a-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="d8d3a-119">MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="d8d3a-119">MsiConfigureServices</span></span>

[<span data-ttu-id="d8d3a-120">StartServices</span><span class="sxs-lookup"><span data-stu-id="d8d3a-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="d8d3a-121">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="d8d3a-121">ActionData Messages</span></span>

<span data-ttu-id="d8d3a-122">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d3a-123">備註</span><span class="sxs-lookup"><span data-stu-id="d8d3a-123">Remarks</span></span>

<span data-ttu-id="d8d3a-124">此動作會要求使用者必須是系統管理員，或擁有具有安裝服務或應用程式屬於受管理安裝之許可權的更高許可權。</span><span class="sxs-lookup"><span data-stu-id="d8d3a-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



