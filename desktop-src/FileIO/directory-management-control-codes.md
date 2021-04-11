---
description: 搭配檔案壓縮和解壓縮以及重新分析點使用的控制代碼。
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: 目錄管理控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851579"
---
# <a name="directory-management-control-codes"></a><span data-ttu-id="e62d0-103">目錄管理控制碼</span><span class="sxs-lookup"><span data-stu-id="e62d0-103">Directory Management Control Codes</span></span>

<span data-ttu-id="e62d0-104">下列控制碼適用于 [檔案壓縮和解壓縮](file-compression-and-decompression.md)。</span><span class="sxs-lookup"><span data-stu-id="e62d0-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="e62d0-105">控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="e62d0-105">Control Code</span></span>                                             | <span data-ttu-id="e62d0-106">意義</span><span class="sxs-lookup"><span data-stu-id="e62d0-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e62d0-107">**FSCTL \_ 取得 \_ 壓縮**</span><span class="sxs-lookup"><span data-stu-id="e62d0-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="e62d0-108">在檔案系統支援每個資料流程壓縮的磁片區上，抓取檔案或目錄的目前壓縮狀態。</span><span class="sxs-lookup"><span data-stu-id="e62d0-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="e62d0-109">**FSCTL \_ 設定 \_ 壓縮**</span><span class="sxs-lookup"><span data-stu-id="e62d0-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="e62d0-110">在檔案系統支援每個檔案和每個目錄壓縮的磁片區上，設定檔案或目錄的壓縮狀態。</span><span class="sxs-lookup"><span data-stu-id="e62d0-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="e62d0-111">下列控制碼會搭配重新 [分析點](reparse-points.md)使用。</span><span class="sxs-lookup"><span data-stu-id="e62d0-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e62d0-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="e62d0-112">In this section</span></span>



| <span data-ttu-id="e62d0-113">控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="e62d0-113">Control Code</span></span>                                                                   | <span data-ttu-id="e62d0-114">Description</span><span class="sxs-lookup"><span data-stu-id="e62d0-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e62d0-115">**FSCTL \_ 刪除重新 \_ 分析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="e62d0-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="e62d0-116">從指定的檔案或目錄中刪除重新分析點。</span><span class="sxs-lookup"><span data-stu-id="e62d0-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="e62d0-117">**FSCTL \_ 取得重新 \_ 剖析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="e62d0-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="e62d0-118">抓取與指定之控制碼所識別之檔案或目錄相關聯的重新分析點資料。</span><span class="sxs-lookup"><span data-stu-id="e62d0-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="e62d0-119">**FSCTL \_ 設定重新 \_ 分析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="e62d0-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="e62d0-120">在檔案或目錄上設定重新分析點。</span><span class="sxs-lookup"><span data-stu-id="e62d0-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e62d0-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e62d0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e62d0-122">檔案管理控制碼</span><span class="sxs-lookup"><span data-stu-id="e62d0-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="e62d0-123">磁碟區管理控制碼</span><span class="sxs-lookup"><span data-stu-id="e62d0-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

