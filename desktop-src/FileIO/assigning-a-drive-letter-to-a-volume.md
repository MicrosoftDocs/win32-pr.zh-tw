---
description: 如果沒有已指派給該磁碟機號的磁片區，您可以使用 SetVolumeMountPoint 函式，將磁碟機號 (例如 X：指派給 \) 本機磁片區。
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: 指派磁碟機號給磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974200"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="8fe5e-103">指派磁碟機號給磁片區</span><span class="sxs-lookup"><span data-stu-id="8fe5e-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="8fe5e-104">如果沒有 \) 已指派給該磁碟機號的磁片區，您可以使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式，將磁碟機號 (例如 X：指派給本機磁片區。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="8fe5e-105">如果本機磁片區已經有磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="8fe5e-106">然後 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="8fe5e-107">若要處理這種情況，請先使用 [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) 函式刪除磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="8fe5e-108">如需範例程式碼，請參閱 [編輯磁碟機號指派](editing-drive-letter-assignments.md)。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="8fe5e-109">系統最多可為每個磁片區支援一個磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="8fe5e-110">因此，您不能有 C： \\ 和 F： \\ 代表相同的磁片區。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="8fe5e-111">刪除現有的磁碟機號並指派新的磁碟機號，可能會中斷現有的路徑，例如桌面快捷方式中的路徑。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="8fe5e-112">它也可能會中斷變更磁碟機號的程式路徑。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="8fe5e-113">使用 Windows 虛擬記憶體管理時，這可能會中斷應用程式，讓系統處於不穩定且可能無法使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="8fe5e-114">程式設計人員必須負責避免這類潛在的最受到自然災害。</span><span class="sxs-lookup"><span data-stu-id="8fe5e-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



