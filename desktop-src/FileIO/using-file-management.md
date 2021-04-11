---
description: 下列範例使用檔案管理功能。
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: 使用檔案管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027332"
---
# <a name="using-file-management"></a><span data-ttu-id="440bf-103">使用檔案管理</span><span class="sxs-lookup"><span data-stu-id="440bf-103">Using File Management</span></span>

<span data-ttu-id="440bf-104">下列範例使用檔案管理功能。</span><span class="sxs-lookup"><span data-stu-id="440bf-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="440bf-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="440bf-105">In this section</span></span>



| <span data-ttu-id="440bf-106">主題</span><span class="sxs-lookup"><span data-stu-id="440bf-106">Topic</span></span>                                                                                                   | <span data-ttu-id="440bf-107">描述</span><span class="sxs-lookup"><span data-stu-id="440bf-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="440bf-108">將使用者新增至加密的檔案</span><span class="sxs-lookup"><span data-stu-id="440bf-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="440bf-109">示範如何使用 [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) 函式，將新的使用者加入現有的加密檔案的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="440bf-110">將一個檔案附加至另一個檔案</span><span class="sxs-lookup"><span data-stu-id="440bf-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="440bf-111">示範應用程式如何將一個檔案附加至另一個檔案結尾的範例程式碼，包括如何開啟和關閉檔案、讀取和寫入檔案，以及鎖定和解除鎖定檔案。</span><span class="sxs-lookup"><span data-stu-id="440bf-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="440bf-112">建立和使用暫存檔案</span><span class="sxs-lookup"><span data-stu-id="440bf-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="440bf-113">示範如何使用 GetTempFileName 和 GetTempPath 函數建立暫存檔案以進行資料操作的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="440bf-114">鎖定和解除鎖定檔案中的位元組範圍</span><span class="sxs-lookup"><span data-stu-id="440bf-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="440bf-115">使用 LockFileEx 和 UnlockFileEx 函數來顯示位元組範圍鎖定和解除鎖定的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="440bf-116">開啟檔案進行讀取或寫入</span><span class="sxs-lookup"><span data-stu-id="440bf-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="440bf-117">示範如何使用 CreateFile 函數建立新檔案或開啟現有檔案的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="440bf-118">取出和變更檔案屬性</span><span class="sxs-lookup"><span data-stu-id="440bf-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="440bf-119">示範如何使用 GetFileAttributesEx 函數來取出檔案屬性的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="440bf-120">測試檔案尾</span><span class="sxs-lookup"><span data-stu-id="440bf-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="440bf-121">示範如何在同步讀取作業期間和非同步讀取作業期間測試檔案尾的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="440bf-122">使用資料流程</span><span class="sxs-lookup"><span data-stu-id="440bf-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="440bf-123">顯示如何使用基本 NTFS 檔案系統資料流程的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="440bf-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




