---
description: NTFS 檔案系統支援兩種類型的連結：永久連結和連接。
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: 檔案和目錄連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945148"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="b16ee-103">檔案和目錄連結</span><span class="sxs-lookup"><span data-stu-id="b16ee-103">File and Directory Linking</span></span>

<span data-ttu-id="b16ee-104">NTFS 檔案系統可讓您在目錄結構中的位置建立檔案或目錄的系統標記法，此結構不同于所連結的檔案或目錄物件。</span><span class="sxs-lookup"><span data-stu-id="b16ee-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="b16ee-105">此進程稱為連結。</span><span class="sxs-lookup"><span data-stu-id="b16ee-105">This process is called linking.</span></span> <span data-ttu-id="b16ee-106">NTFS 檔案系統支援兩種類型的連結：永久 [連結和](hard-links-and-junctions.md)連接。</span><span class="sxs-lookup"><span data-stu-id="b16ee-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="b16ee-107">NTFS 檔案系統也提供 [分散式連結追蹤服務](distributed-link-tracking-and-object-identifiers.md)，其會在連結移動時自動追蹤連結。</span><span class="sxs-lookup"><span data-stu-id="b16ee-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b16ee-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="b16ee-108">In this section</span></span>



| <span data-ttu-id="b16ee-109">主題</span><span class="sxs-lookup"><span data-stu-id="b16ee-109">Topic</span></span>                                                                                                               | <span data-ttu-id="b16ee-110">描述</span><span class="sxs-lookup"><span data-stu-id="b16ee-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b16ee-111">永久連結和接合</span><span class="sxs-lookup"><span data-stu-id="b16ee-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="b16ee-112">描述永久連結和接合。</span><span class="sxs-lookup"><span data-stu-id="b16ee-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="b16ee-113">分散式連結追蹤和物件識別碼</span><span class="sxs-lookup"><span data-stu-id="b16ee-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="b16ee-114">**分散式連結追蹤服務** 可讓用戶端應用程式追蹤已移動的連結來源。</span><span class="sxs-lookup"><span data-stu-id="b16ee-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




