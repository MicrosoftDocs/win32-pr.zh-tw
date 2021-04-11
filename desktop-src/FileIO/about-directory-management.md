---
description: 包含一或多個目錄的目錄是包含的目錄或目錄的父系，而每個包含的目錄都是父目錄的子系。 目錄的階層式結構稱為目錄樹狀目錄。
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: 關於目錄管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848061"
---
# <a name="about-directory-management"></a><span data-ttu-id="9b384-104">關於目錄管理</span><span class="sxs-lookup"><span data-stu-id="9b384-104">About Directory Management</span></span>

<span data-ttu-id="9b384-105">包含一或多個目錄的目錄是包含的目錄或目錄的 *父系* ，而每個包含的目錄都是父目錄的 *子* 系。</span><span class="sxs-lookup"><span data-stu-id="9b384-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="9b384-106">目錄的階層式結構稱為 *目錄樹狀目錄*。</span><span class="sxs-lookup"><span data-stu-id="9b384-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="9b384-107">NTFS 檔案系統會將目錄和其所包含之檔案之間的邏輯連結，實作為 *目錄專案資料表*。</span><span class="sxs-lookup"><span data-stu-id="9b384-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="9b384-108">當檔案移至目錄時，會在表格中為移動的檔案建立一個專案，並將該檔案的名稱放在專案中。</span><span class="sxs-lookup"><span data-stu-id="9b384-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="9b384-109">當刪除包含在目錄中的檔案時，也會從資料表中刪除對應至已刪除檔案的名稱和專案。</span><span class="sxs-lookup"><span data-stu-id="9b384-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="9b384-110">目錄專案資料表中可以有一個以上的單一檔案專案。</span><span class="sxs-lookup"><span data-stu-id="9b384-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="9b384-111">如果在資料表中為檔案建立額外的專案，該專案就稱為該檔案的永久 *連結* 。</span><span class="sxs-lookup"><span data-stu-id="9b384-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="9b384-112">可以為單一檔案建立的永久連結數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="9b384-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="9b384-113">目錄也可以包含聯接和重新分析點。</span><span class="sxs-lookup"><span data-stu-id="9b384-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b384-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="9b384-114">In this section</span></span>



| <span data-ttu-id="9b384-115">主題</span><span class="sxs-lookup"><span data-stu-id="9b384-115">Topic</span></span>                                                                                 | <span data-ttu-id="9b384-116">描述</span><span class="sxs-lookup"><span data-stu-id="9b384-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b384-117">建立和刪除目錄</span><span class="sxs-lookup"><span data-stu-id="9b384-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="9b384-118">應用程式可透過程式設計方式建立和刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="9b384-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="9b384-119">目錄控制碼</span><span class="sxs-lookup"><span data-stu-id="9b384-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="9b384-120">只要進程建立或開啟目錄物件，它就會收到物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9b384-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="9b384-121">重新剖析點</span><span class="sxs-lookup"><span data-stu-id="9b384-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="9b384-122">描述重新分析點。</span><span class="sxs-lookup"><span data-stu-id="9b384-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="9b384-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b384-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b384-124">目錄管理參考</span><span class="sxs-lookup"><span data-stu-id="9b384-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




