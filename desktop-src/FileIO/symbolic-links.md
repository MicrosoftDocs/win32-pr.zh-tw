---
description: 符號連結是指向另一個檔案系統物件的檔案系統物件。 所指向的物件稱為「目標」。
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: 符號連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994465"
---
# <a name="symbolic-links"></a><span data-ttu-id="a0773-104">符號連結</span><span class="sxs-lookup"><span data-stu-id="a0773-104">Symbolic Links</span></span>

<span data-ttu-id="a0773-105">符號連結是指向另一個檔案系統物件的檔案系統物件。</span><span class="sxs-lookup"><span data-stu-id="a0773-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="a0773-106">所指向的物件稱為「目標」。</span><span class="sxs-lookup"><span data-stu-id="a0773-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="a0773-107">符號連結對使用者而言是透明的;這些連結會顯示為一般檔案或目錄，並可由使用者或應用程式以完全相同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="a0773-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="a0773-108">符號連結是設計來協助與 UNIX 作業系統進行遷移和應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="a0773-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="a0773-109">Microsoft 已實作為其符號連結的運作方式，就像 UNIX 連結一樣。</span><span class="sxs-lookup"><span data-stu-id="a0773-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="a0773-110">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="a0773-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0773-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="a0773-111">In this section</span></span>



| <span data-ttu-id="a0773-112">主題</span><span class="sxs-lookup"><span data-stu-id="a0773-112">Topic</span></span>                                                                                                             | <span data-ttu-id="a0773-113">描述</span><span class="sxs-lookup"><span data-stu-id="a0773-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0773-114">檔案系統函數的符號連結效果</span><span class="sxs-lookup"><span data-stu-id="a0773-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="a0773-115">符號連結如何影響使用路徑名稱來指定一個或多個檔案的標準檔案函數。</span><span class="sxs-lookup"><span data-stu-id="a0773-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="a0773-116">程式設計考量</span><span class="sxs-lookup"><span data-stu-id="a0773-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="a0773-117">使用符號連結的程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="a0773-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="a0773-118">建立符號連結</span><span class="sxs-lookup"><span data-stu-id="a0773-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="a0773-119">使用 [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) 函數建立使用絕對或相對路徑的符號連結。</span><span class="sxs-lookup"><span data-stu-id="a0773-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="a0773-120">支援的作業系統</span><span class="sxs-lookup"><span data-stu-id="a0773-120">Supported Operating Systems</span></span>

<span data-ttu-id="a0773-121">從 Windows Vista 開始，NTFS 提供符號連結。</span><span class="sxs-lookup"><span data-stu-id="a0773-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




