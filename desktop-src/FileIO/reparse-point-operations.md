---
description: 描述您可以使用 DeviceIoControl 執行的重新分析點作業。
ms.assetid: c7279203-2443-401e-b541-038954094266
title: 重新分析點作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027258"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="5782f-103">重新分析點作業</span><span class="sxs-lookup"><span data-stu-id="5782f-103">Reparse Point Operations</span></span>

<span data-ttu-id="5782f-104">若要判斷檔案系統是否支援重新分析點，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式，並檢查檔案是否 **支援重新 \_ \_ 分析 \_ 點** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="5782f-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="5782f-105">[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數可讓您設定、修改、取得和移除重新分析點。</span><span class="sxs-lookup"><span data-stu-id="5782f-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="5782f-106">下表描述您可以使用 **DeviceIoControl** 執行的重新分析點作業。</span><span class="sxs-lookup"><span data-stu-id="5782f-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="5782f-107">作業</span><span class="sxs-lookup"><span data-stu-id="5782f-107">Operation</span></span>                                                           | <span data-ttu-id="5782f-108">描述</span><span class="sxs-lookup"><span data-stu-id="5782f-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5782f-109">**FSCTL \_ 設定重新 \_ 分析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="5782f-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="5782f-110">允許呼叫程式設定新的重新分析點，或修改現有的重新分析點。</span><span class="sxs-lookup"><span data-stu-id="5782f-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="5782f-111">**FSCTL \_ 取得重新 \_ 剖析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="5782f-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="5782f-112">取得儲存在現有重新分析點中的資訊。</span><span class="sxs-lookup"><span data-stu-id="5782f-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="5782f-113">**FSCTL \_ 刪除重新 \_ 分析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="5782f-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="5782f-114">移除現有的重新分析點。</span><span class="sxs-lookup"><span data-stu-id="5782f-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="5782f-115">如果您要修改、取得或刪除重新分析點，您必須在檔案所包含的作業中指定相同的重新分析標記。</span><span class="sxs-lookup"><span data-stu-id="5782f-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="5782f-116">否則，作業將會失敗，並出現錯誤重新 **\_ 分析 \_ 標記 \_ 不符** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5782f-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="5782f-117">如果您要修改或刪除重新分析點，您也必須在檔案所包含的作業中指定重新分析 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="5782f-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="5782f-118">否則，作業將會失敗，並出現錯誤重新 **\_ 分析 \_ 屬性 \_ 衝突**。</span><span class="sxs-lookup"><span data-stu-id="5782f-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="5782f-119">若要判斷檔案或目錄是否包含重新分析點，請使用 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函數。</span><span class="sxs-lookup"><span data-stu-id="5782f-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="5782f-120">如果檔案或目錄有相關聯的重新分析點，則會設定 **檔 \_ 屬性重新 \_ 分析 \_ 點** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5782f-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="5782f-121">若要覆寫現有的重新分析點，而不使用檔案或目錄的控制碼，請使用檔案 **\_ 旗標開啟重新 \_ \_ 分析 \_ 點** 來呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 。</span><span class="sxs-lookup"><span data-stu-id="5782f-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="5782f-122">這個旗標可讓您開啟檔案，無論對應的檔案系統篩選器是否已安裝且正常運作。</span><span class="sxs-lookup"><span data-stu-id="5782f-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 

