---
description: 描述重新分析點。
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: 重新剖析點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851364"
---
# <a name="reparse-points"></a><span data-ttu-id="0aa92-103">重新剖析點</span><span class="sxs-lookup"><span data-stu-id="0aa92-103">Reparse Points</span></span>

<span data-ttu-id="0aa92-104">檔案或目錄可以包含重新 *分析點*，這是使用者定義資料的集合。</span><span class="sxs-lookup"><span data-stu-id="0aa92-104">A file or directory can contain a *reparse point*, which is a collection of user-defined data.</span></span> <span data-ttu-id="0aa92-105">儲存資料的應用程式會瞭解這項資料的格式，以及您安裝來解讀資料和處理檔案的檔案系統篩選器。</span><span class="sxs-lookup"><span data-stu-id="0aa92-105">The format of this data is understood by the application which stores the data, and a file system filter, which you install to interpret the data and process the file.</span></span> <span data-ttu-id="0aa92-106">當應用程式設定重新分析點時，它會儲存這項資料，加上重新 *分析標記*，可唯一識別它所儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="0aa92-106">When an application sets a reparse point, it stores this data, plus a *reparse tag*, which uniquely identifies the data it is storing.</span></span> <span data-ttu-id="0aa92-107">當檔案系統開啟具有重新分析點的檔案時，它會嘗試尋找與重新分析標記所識別之資料格式相關聯的檔案系統篩選器。</span><span class="sxs-lookup"><span data-stu-id="0aa92-107">When the file system opens a file with a reparse point, it attempts to find the file system filter associated with the data format identified by the reparse tag.</span></span> <span data-ttu-id="0aa92-108">如果找到檔案系統篩選器，則篩選會依重新分析資料的指示處理檔案。</span><span class="sxs-lookup"><span data-stu-id="0aa92-108">If a file system filter is found, the filter processes the file as directed by the reparse data.</span></span> <span data-ttu-id="0aa92-109">如果找不到檔案系統篩選器，則檔案開啟作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="0aa92-109">If a file system filter is not found, the file open operation fails.</span></span>

<span data-ttu-id="0aa92-110">例如，重新分析點用來執行 NTFS 檔案系統連結和 Microsoft 遠端存放伺服器 (RSS) 。</span><span class="sxs-lookup"><span data-stu-id="0aa92-110">For example, reparse points are used to implement NTFS file system links and the Microsoft Remote Storage Server (RSS).</span></span> <span data-ttu-id="0aa92-111">RSS 使用一組系統管理員定義的規則，將不常使用的檔案移至長期儲存，例如磁帶或光學媒體。</span><span class="sxs-lookup"><span data-stu-id="0aa92-111">RSS uses an administrator-defined set of rules to move infrequently used files to long term storage, such as tape or optical media.</span></span> <span data-ttu-id="0aa92-112">它會使用重新分析點來儲存檔案系統中檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0aa92-112">It uses reparse points to store information about the file in the file system.</span></span> <span data-ttu-id="0aa92-113">這項資訊會儲存在包含重新分析點的存根檔中，而該重新分析點的資料會指向實際檔案目前所在的裝置。</span><span class="sxs-lookup"><span data-stu-id="0aa92-113">This information is stored in a stub file that contains a reparse point whose data points to the device where the actual file is now located.</span></span> <span data-ttu-id="0aa92-114">檔案系統篩選器可以使用此資訊來取出檔案。</span><span class="sxs-lookup"><span data-stu-id="0aa92-114">The file system filter can use this information to retrieve the file.</span></span>

<span data-ttu-id="0aa92-115">重新分析點也會用來執行裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0aa92-115">Reparse points are also used to implement mounted folders.</span></span> <span data-ttu-id="0aa92-116">如需詳細資訊，請參閱 [判斷目錄是否為裝載的資料夾](determining-whether-a-directory-is-a-volume-mount-point.md)。</span><span class="sxs-lookup"><span data-stu-id="0aa92-116">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>

<span data-ttu-id="0aa92-117">下列限制適用于重新分析點：</span><span class="sxs-lookup"><span data-stu-id="0aa92-117">The following restrictions apply to reparse points:</span></span>

-   <span data-ttu-id="0aa92-118">您可以建立目錄的重新分析點，但目錄必須是空的。</span><span class="sxs-lookup"><span data-stu-id="0aa92-118">Reparse points can be established for a directory, but the directory must be empty.</span></span> <span data-ttu-id="0aa92-119">否則，NTFS 檔案系統將無法建立重新分析點。</span><span class="sxs-lookup"><span data-stu-id="0aa92-119">Otherwise, the NTFS file system fails to establish the reparse point.</span></span> <span data-ttu-id="0aa92-120">此外，您無法在包含重新分析點的目錄中建立目錄或檔案。</span><span class="sxs-lookup"><span data-stu-id="0aa92-120">In addition, you cannot create directories or files in a directory that contains a reparse point.</span></span>
-   <span data-ttu-id="0aa92-121">重新分析點和擴充屬性互斥。</span><span class="sxs-lookup"><span data-stu-id="0aa92-121">Reparse points and extended attributes are mutually exclusive.</span></span> <span data-ttu-id="0aa92-122">當檔案包含擴充屬性時，NTFS 檔案系統無法建立重新分析點，而且無法在包含重新分析點的檔案上建立擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="0aa92-122">The NTFS file system cannot create a reparse point when the file contains extended attributes, and it cannot create extended attributes on a file that contains a reparse point.</span></span>
-   <span data-ttu-id="0aa92-123">重新分析點資料（包括標記和選用的 **GUID**）不能超過 16 kb。</span><span class="sxs-lookup"><span data-stu-id="0aa92-123">Reparse point data, including the tag and optional **GUID**, cannot exceed 16 kilobytes.</span></span> <span data-ttu-id="0aa92-124">如果要在重新分析點中放置的資料量超過此限制，則設定重新分析點會失敗。</span><span class="sxs-lookup"><span data-stu-id="0aa92-124">Setting a reparse point fails if the amount of data to be placed in the reparse point exceeds this limit.</span></span>
-   <span data-ttu-id="0aa92-125">在任何指定的路徑上，都有63重新分析點的限制。</span><span class="sxs-lookup"><span data-stu-id="0aa92-125">There is a limit of 63 reparse points on any given path.</span></span>

    <span data-ttu-id="0aa92-126">**Windows Server 2003 和 WINDOWS XP：** 在任何指定的路徑上，都有31個重新分析點的限制。</span><span class="sxs-lookup"><span data-stu-id="0aa92-126">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0aa92-127">本節內容</span><span class="sxs-lookup"><span data-stu-id="0aa92-127">In this section</span></span>



| <span data-ttu-id="0aa92-128">主題</span><span class="sxs-lookup"><span data-stu-id="0aa92-128">Topic</span></span>                                                                                   | <span data-ttu-id="0aa92-129">描述</span><span class="sxs-lookup"><span data-stu-id="0aa92-129">Description</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aa92-130">重新分析點標記</span><span class="sxs-lookup"><span data-stu-id="0aa92-130">Reparse Point Tags</span></span>](reparse-point-tags.md)<br/>                                 | <span data-ttu-id="0aa92-131">每個重新分析點都有一個識別碼標記，如此您就可以有效率地區分不同類型的重新分析點，而不需要檢查重新分析點中的使用者定義資料。</span><span class="sxs-lookup"><span data-stu-id="0aa92-131">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span><br/> |
| [<span data-ttu-id="0aa92-132">重新分析點作業</span><span class="sxs-lookup"><span data-stu-id="0aa92-132">Reparse Point Operations</span></span>](reparse-point-operations.md)<br/>                     | <span data-ttu-id="0aa92-133">描述您可以使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)執行的重新分析點作業。</span><span class="sxs-lookup"><span data-stu-id="0aa92-133">Describes the reparse point operations that you can perform by using [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span><br/>                                                                                       |
| [<span data-ttu-id="0aa92-134">重新分析點和檔案作業</span><span class="sxs-lookup"><span data-stu-id="0aa92-134">Reparse Points and File Operations</span></span>](reparse-points-and-file-operations.md)<br/> | <span data-ttu-id="0aa92-135">描述重新剖析點如何啟用從大部分 Windows 開發人員預期的行為離開的檔案系統行為。</span><span class="sxs-lookup"><span data-stu-id="0aa92-135">Describes how reparse points enable file system behavior that departs from behavior most Windows developers expect.</span></span><br/>                                                                                     |



 

 

