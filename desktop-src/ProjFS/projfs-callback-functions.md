---
title: ProjFS 回呼函式
description: 下列回呼函數是在 projectedfslib 中宣告。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2020
ms.locfileid: "103841827"
---
# <a name="callback-functions"></a><span data-ttu-id="e0dda-103">回呼函數</span><span class="sxs-lookup"><span data-stu-id="e0dda-103">Callback functions</span></span>

<span data-ttu-id="e0dda-104">下列回呼函數是在 projectedfslib 中宣告。</span><span class="sxs-lookup"><span data-stu-id="e0dda-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e0dda-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e0dda-105">In this section</span></span>

| <span data-ttu-id="e0dda-106">主題</span><span class="sxs-lookup"><span data-stu-id="e0dda-106">Topic</span></span> | <span data-ttu-id="e0dda-107">描述</span><span class="sxs-lookup"><span data-stu-id="e0dda-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="e0dda-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="e0dda-109">通知提供者，先前調用回呼的作業應該取消。</span><span class="sxs-lookup"><span data-stu-id="e0dda-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="e0dda-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="e0dda-111">通知提供者目錄列舉已結束。</span><span class="sxs-lookup"><span data-stu-id="e0dda-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="e0dda-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="e0dda-113">從提供者要求目錄列舉資訊。</span><span class="sxs-lookup"><span data-stu-id="e0dda-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="e0dda-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="e0dda-115">要求檔案主要資料流程的內容。</span><span class="sxs-lookup"><span data-stu-id="e0dda-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="e0dda-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="e0dda-117">從提供者要求檔案或目錄的資訊。</span><span class="sxs-lookup"><span data-stu-id="e0dda-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="e0dda-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="e0dda-119">將檔案系統作業的通知傳送給提供者。</span><span class="sxs-lookup"><span data-stu-id="e0dda-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="e0dda-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="e0dda-121">判斷指定的檔案路徑是否存在於提供者的備份存放區中。</span><span class="sxs-lookup"><span data-stu-id="e0dda-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="e0dda-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="e0dda-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="e0dda-123">通知提供者目錄列舉正在啟動。</span><span class="sxs-lookup"><span data-stu-id="e0dda-123">Informs the provider that a directory enumeration is starting.</span></span>