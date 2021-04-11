---
description: 用來管理裝載資料夾的函式。
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: 裝載的資料夾函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319408"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="8125e-103">裝載的資料夾函式</span><span class="sxs-lookup"><span data-stu-id="8125e-103">Mounted Folder Functions</span></span>

<span data-ttu-id="8125e-104">裝載的資料夾功能可以分為三個群組：一般用途的函式、用來掃描磁片區的函式，以及用來掃描磁片區是否有載入的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8125e-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="8125e-105">General-Purpose 載入的資料夾函式</span><span class="sxs-lookup"><span data-stu-id="8125e-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="8125e-106">函式</span><span class="sxs-lookup"><span data-stu-id="8125e-106">Function</span></span>                                                                     | <span data-ttu-id="8125e-107">描述</span><span class="sxs-lookup"><span data-stu-id="8125e-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8125e-108">**DeleteVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="8125e-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="8125e-109">刪除磁碟機號或掛接的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8125e-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="8125e-110">**GetVolumeNameForVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="8125e-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="8125e-111">抓取與指定磁片區掛接點相關聯之磁片區的磁片區 GUID 路徑 (磁碟機號、磁片區 GUID 路徑，或已載入的資料夾) 。</span><span class="sxs-lookup"><span data-stu-id="8125e-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="8125e-112">**GetVolumePathName**</span><span class="sxs-lookup"><span data-stu-id="8125e-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="8125e-113">抓取與指定磁片區相關聯的已掛接資料夾。</span><span class="sxs-lookup"><span data-stu-id="8125e-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="8125e-114">**SetVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="8125e-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="8125e-115">將磁片區與磁碟機號或另一個磁片區上的目錄產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8125e-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="8125e-116">Volume-Scanning 函式</span><span class="sxs-lookup"><span data-stu-id="8125e-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="8125e-117">函式</span><span class="sxs-lookup"><span data-stu-id="8125e-117">Function</span></span>                                   | <span data-ttu-id="8125e-118">描述</span><span class="sxs-lookup"><span data-stu-id="8125e-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8125e-119">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="8125e-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="8125e-120">傳回電腦上的磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="8125e-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="8125e-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) 可用來開始列舉電腦的磁片區。</span><span class="sxs-lookup"><span data-stu-id="8125e-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="8125e-122">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="8125e-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="8125e-123">繼續呼叫 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)來開始進行磁片區搜尋。</span><span class="sxs-lookup"><span data-stu-id="8125e-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="8125e-124">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="8125e-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="8125e-125">關閉磁片區的搜尋。</span><span class="sxs-lookup"><span data-stu-id="8125e-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="8125e-126">載入的資料夾掃描功能</span><span class="sxs-lookup"><span data-stu-id="8125e-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="8125e-127">函式</span><span class="sxs-lookup"><span data-stu-id="8125e-127">Function</span></span>                                                       | <span data-ttu-id="8125e-128">描述</span><span class="sxs-lookup"><span data-stu-id="8125e-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8125e-129">**FindFirstVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="8125e-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="8125e-130">抓取指定磁片區上所裝載的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="8125e-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="8125e-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) 可用來開始掃描磁片區上掛接的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8125e-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="8125e-132">**FindNextVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="8125e-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="8125e-133">繼續呼叫 [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)來開始載入的資料夾搜尋。</span><span class="sxs-lookup"><span data-stu-id="8125e-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="8125e-134">**FindVolumeMountPointClose**</span><span class="sxs-lookup"><span data-stu-id="8125e-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="8125e-135">關閉已載入資料夾的搜尋。</span><span class="sxs-lookup"><span data-stu-id="8125e-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



