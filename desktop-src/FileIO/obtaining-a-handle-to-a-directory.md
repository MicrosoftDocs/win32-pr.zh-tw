---
description: 只要進程建立或開啟目錄物件，它就會收到物件的控制碼。
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: 目錄控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987821"
---
# <a name="directory-handles"></a><span data-ttu-id="64d8e-103">目錄控制碼</span><span class="sxs-lookup"><span data-stu-id="64d8e-103">Directory Handles</span></span>

<span data-ttu-id="64d8e-104">只要進程建立或開啟目錄物件，它就會收到物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="64d8e-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="64d8e-105">若要取得現有目錄的控制碼，請使用檔案 **\_ 旗標 \_ 備份 \_ 語義** 旗標來呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函數。</span><span class="sxs-lookup"><span data-stu-id="64d8e-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="64d8e-106">您可以將目錄控制碼傳遞給下列函式。</span><span class="sxs-lookup"><span data-stu-id="64d8e-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="64d8e-107">函式</span><span class="sxs-lookup"><span data-stu-id="64d8e-107">Function</span></span>                                                         | <span data-ttu-id="64d8e-108">描述</span><span class="sxs-lookup"><span data-stu-id="64d8e-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64d8e-109">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="64d8e-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="64d8e-110">備份檔案或目錄，包括安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="64d8e-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="64d8e-111">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="64d8e-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="64d8e-112">在一開始使用 [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) 或 [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) 函數來存取資料流程時，向前搜尋。</span><span class="sxs-lookup"><span data-stu-id="64d8e-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="64d8e-113">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="64d8e-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="64d8e-114">還原使用 [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)備份的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="64d8e-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="64d8e-115">**GetFileInformationByHandle**</span><span class="sxs-lookup"><span data-stu-id="64d8e-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="64d8e-116">抓取指定檔案的檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="64d8e-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="64d8e-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="64d8e-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="64d8e-118">捕獲指定檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="64d8e-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="64d8e-119">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="64d8e-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="64d8e-120">抓取檔案或目錄的建立日期和時間、上次存取的時間，以及上次修改的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="64d8e-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="64d8e-121">**GetFileType**</span><span class="sxs-lookup"><span data-stu-id="64d8e-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="64d8e-122">抓取指定之檔案的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="64d8e-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="64d8e-123">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="64d8e-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="64d8e-124">抓取描述指定目錄內變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="64d8e-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="64d8e-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="64d8e-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="64d8e-126">設定指定檔案或目錄的建立日期和時間、上次存取時間或上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="64d8e-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

