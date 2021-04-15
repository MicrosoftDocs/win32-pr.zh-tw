---
title: 磁帶初始化
description: 應用程式必須使用 CreateFile 函式來建立磁帶裝置的控制碼。 此控制碼用於裝置中磁帶的後續作業。
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- 磁帶初始化備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463425"
---
# <a name="tape-initialization"></a><span data-ttu-id="fe8a7-105">磁帶初始化</span><span class="sxs-lookup"><span data-stu-id="fe8a7-105">Tape Initialization</span></span>

<span data-ttu-id="fe8a7-106">應用程式必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來建立磁帶裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="fe8a7-107">此控制碼用於裝置中磁帶的後續作業。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="fe8a7-108">在應用程式寫入磁帶之前，必須根據應用程式的需求以及使用的磁帶機功能來格式化磁帶。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="fe8a7-109">[**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition)函式會重新格式化磁帶，在其上建立指定大小的指定磁碟分割數目。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="fe8a7-110">[**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)函數會準備要存取或移除的磁帶。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="fe8a7-111">此函數可以載入、卸載、鎖定或解除鎖定磁帶。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="fe8a7-112">此函式也可以將磁帶移至磁帶的結尾，再回到開頭，以將磁帶張力。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="fe8a7-113">若要抓取和設定磁帶和磁帶機的相關資訊，應用程式會使用 [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)、 [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)和 [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) 功能。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="fe8a7-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) 會取出描述磁帶或磁帶機的資訊。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="fe8a7-115">磁帶資訊包含磁帶的類型、密度和區塊大小;磁帶上的磁碟分割數目;剩餘的磁帶數量;依此類推。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="fe8a7-116">磁帶機資訊包括磁片磁碟機的預設區塊大小、最大分割區計數，以及支援的功能。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="fe8a7-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) 會設定磁帶區塊大小或設定磁帶機旗標，以指出磁片磁碟機是否支援硬體錯誤修正、資料壓縮、資料填補或三種組合。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="fe8a7-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) 指出磁帶機是否已準備好處理磁帶命令。</span><span class="sxs-lookup"><span data-stu-id="fe8a7-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 