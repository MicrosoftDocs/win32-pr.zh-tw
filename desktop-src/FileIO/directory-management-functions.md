---
description: 目錄管理中使用的函數。
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: 目錄管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194401"
---
# <a name="directory-management-functions"></a><span data-ttu-id="2e597-103">目錄管理功能</span><span class="sxs-lookup"><span data-stu-id="2e597-103">Directory Management Functions</span></span>

<span data-ttu-id="2e597-104">目錄管理中會使用下列功能。</span><span class="sxs-lookup"><span data-stu-id="2e597-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e597-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="2e597-105">In this section</span></span>



| <span data-ttu-id="2e597-106">函式</span><span class="sxs-lookup"><span data-stu-id="2e597-106">Function</span></span>                                                                      | <span data-ttu-id="2e597-107">描述</span><span class="sxs-lookup"><span data-stu-id="2e597-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e597-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="2e597-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="2e597-109">建立新目錄。</span><span class="sxs-lookup"><span data-stu-id="2e597-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="2e597-110">**CreateDirectoryEx**</span><span class="sxs-lookup"><span data-stu-id="2e597-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="2e597-111">使用指定之範本目錄的屬性，建立新的目錄。</span><span class="sxs-lookup"><span data-stu-id="2e597-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="2e597-112">**CreateDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="2e597-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="2e597-113">使用指定範本目錄的屬性，建立新目錄做為交易作業。</span><span class="sxs-lookup"><span data-stu-id="2e597-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="2e597-114">**FindCloseChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2e597-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="2e597-115">停止變更通知控制碼監視。</span><span class="sxs-lookup"><span data-stu-id="2e597-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="2e597-116">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2e597-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="2e597-117">建立變更通知控制碼，並設定初始變更通知篩選準則。</span><span class="sxs-lookup"><span data-stu-id="2e597-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="2e597-118">**FindNextChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2e597-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="2e597-119">要求作業系統在下次偵測到適當的變更時，發出變更通知處理。</span><span class="sxs-lookup"><span data-stu-id="2e597-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="2e597-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="2e597-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="2e597-121">抓取目前進程的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="2e597-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2e597-122">**ReadDirectoryChangesExW**</span><span class="sxs-lookup"><span data-stu-id="2e597-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="2e597-123">抓取描述指定目錄內之變更的資訊，如果指定了該資訊類型，就可以包含擴充資訊。</span><span class="sxs-lookup"><span data-stu-id="2e597-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="2e597-124">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="2e597-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="2e597-125">抓取描述指定目錄內變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e597-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="2e597-126">**RemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="2e597-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="2e597-127">刪除現有的空白目錄。</span><span class="sxs-lookup"><span data-stu-id="2e597-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="2e597-128">**RemoveDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="2e597-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="2e597-129">將現有的空白目錄刪除為交易作業。</span><span class="sxs-lookup"><span data-stu-id="2e597-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="2e597-130">**>setcurrentdirectory**</span><span class="sxs-lookup"><span data-stu-id="2e597-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="2e597-131">變更目前進程的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="2e597-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




