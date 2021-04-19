---
description: 若要在電腦上建立磁片區的完整清單，或輪流操作每個磁片區，您可以列舉磁片區。
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: 列舉磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975756"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="cd40c-103">列舉磁片區</span><span class="sxs-lookup"><span data-stu-id="cd40c-103">Enumerating Volumes</span></span>

<span data-ttu-id="cd40c-104">若要在電腦上建立磁片區的完整清單，或輪流操作每個磁片區，您可以列舉磁片區。</span><span class="sxs-lookup"><span data-stu-id="cd40c-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="cd40c-105">在磁片區中，您可以掃描磁片區上 [裝載的資料夾](enumerating-volume-mount-points.md) 或其他物件。</span><span class="sxs-lookup"><span data-stu-id="cd40c-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="cd40c-106">有三個功能可讓應用程式列舉電腦上的磁片區：</span><span class="sxs-lookup"><span data-stu-id="cd40c-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="cd40c-107">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="cd40c-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="cd40c-108">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="cd40c-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="cd40c-109">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="cd40c-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="cd40c-110">這三個函式的運作方式非常類似 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數。</span><span class="sxs-lookup"><span data-stu-id="cd40c-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="cd40c-111">開始使用 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)來搜尋磁片區。</span><span class="sxs-lookup"><span data-stu-id="cd40c-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="cd40c-112">如果搜尋成功，請根據應用程式的設計來處理結果。</span><span class="sxs-lookup"><span data-stu-id="cd40c-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="cd40c-113">然後，在迴圈中使用 [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) 來找出並處理每個後續的磁片區。</span><span class="sxs-lookup"><span data-stu-id="cd40c-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="cd40c-114">當磁片區的供應時間用盡時，請關閉 [使用 [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)搜尋]。</span><span class="sxs-lookup"><span data-stu-id="cd40c-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="cd40c-115">您不應該假設這些函式所傳回之磁片區的順序與其他函式或工具傳回的磁片區順序之間的任何關聯性。</span><span class="sxs-lookup"><span data-stu-id="cd40c-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="cd40c-116">尤其是，如果有任何) 或磁片系統管理員，則不會假設 (的磁片區順序和磁碟機號之間的任何關聯性，以及 BIOS 所指派的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="cd40c-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="cd40c-117">如需如何列舉電腦上的磁片區的範例，請參閱 [裝載的資料夾範例](volume-mount-point-examples.md) 。</span><span class="sxs-lookup"><span data-stu-id="cd40c-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



