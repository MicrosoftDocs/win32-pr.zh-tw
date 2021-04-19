---
description: InstallServices 動作會為系統註冊服務。 此動作會查詢 ServiceInstall 資料表。
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: InstallServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975900"
---
# <a name="installservices-action"></a><span data-ttu-id="41479-104">InstallServices 動作</span><span class="sxs-lookup"><span data-stu-id="41479-104">InstallServices Action</span></span>

<span data-ttu-id="41479-105">InstallServices 動作會為系統註冊服務。</span><span class="sxs-lookup"><span data-stu-id="41479-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="41479-106">此動作會查詢 [ServiceInstall 資料表](serviceinstall-table.md)。</span><span class="sxs-lookup"><span data-stu-id="41479-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="41479-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="41479-107">Sequence Restrictions</span></span>

<span data-ttu-id="41479-108">服務動作必須以下列順序使用。</span><span class="sxs-lookup"><span data-stu-id="41479-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="41479-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="41479-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="41479-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="41479-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="41479-111">下列任何一個動作： [InstallFiles](installfiles-action.md)、 [RemoveFiles](removefiles-action.md)、 [DuplicateFiles](duplicatefiles-action.md)、 [MoveFiles](movefiles-action.md)、 [PatchFiles](patchfiles-action.md)和 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="41479-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="41479-112">InstallServices</span><span class="sxs-lookup"><span data-stu-id="41479-112">InstallServices</span></span>

[<span data-ttu-id="41479-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="41479-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="41479-114">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="41479-114">ActionData Messages</span></span>

<span data-ttu-id="41479-115">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="41479-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="41479-116">備註</span><span class="sxs-lookup"><span data-stu-id="41479-116">Remarks</span></span>

<span data-ttu-id="41479-117">此動作會要求使用者必須是系統管理員，或擁有具有安裝服務或應用程式屬於受管理安裝之許可權的更高許可權。</span><span class="sxs-lookup"><span data-stu-id="41479-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



