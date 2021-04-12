---
title: ProjFS 結構
description: 下列結構是在 projectedfslib 中宣告。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 0bf72bd479e273c6c8cbdaa9ed588625298f4f95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104187265"
---
# <a name="projfs-structures"></a><span data-ttu-id="e8e56-103">ProjFS 結構</span><span class="sxs-lookup"><span data-stu-id="e8e56-103">ProjFS structures</span></span>

<span data-ttu-id="e8e56-104">下列結構是在 projectedfslib 中宣告。</span><span class="sxs-lookup"><span data-stu-id="e8e56-104">The following structures are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e8e56-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e8e56-105">In this section</span></span>

| <span data-ttu-id="e8e56-106">主題</span><span class="sxs-lookup"><span data-stu-id="e8e56-106">Topic</span></span> | <span data-ttu-id="e8e56-107">描述</span><span class="sxs-lookup"><span data-stu-id="e8e56-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="e8e56-108">**PRJ_CALLBACK_DATA**</span><span class="sxs-lookup"><span data-stu-id="e8e56-108">**PRJ_CALLBACK_DATA**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_callback_data) | <span data-ttu-id="e8e56-109">針對每個作業回呼，定義傳遞給提供者的標準資訊。</span><span class="sxs-lookup"><span data-stu-id="e8e56-109">Defines the standard information passed to a provider for every operation callback.</span></span> |
| [<span data-ttu-id="e8e56-110">**PRJ_CALLBACKS**</span><span class="sxs-lookup"><span data-stu-id="e8e56-110">**PRJ_CALLBACKS**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_callbacks) | <span data-ttu-id="e8e56-111">一組指標，可讓提供者儲存其回呼常式的實作為位置。</span><span class="sxs-lookup"><span data-stu-id="e8e56-111">A set of pointers to where the provider stores its implementations of the callback routines.</span></span> |
| [<span data-ttu-id="e8e56-112">**PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="e8e56-112">**PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_complete_command_extended_parameters) | <span data-ttu-id="e8e56-113">指定完成某些回呼所需的參數。</span><span class="sxs-lookup"><span data-stu-id="e8e56-113">Specifies parameters required for completing certain callbacks.</span></span> |
| [<span data-ttu-id="e8e56-114">**PRJ_FILE_BASIC_INFO**</span><span class="sxs-lookup"><span data-stu-id="e8e56-114">**PRJ_FILE_BASIC_INFO**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info) | <span data-ttu-id="e8e56-115">專案的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="e8e56-115">Basic information about an item.</span></span> |
| [<span data-ttu-id="e8e56-116">**PRJ_NOTIFICATION_MAPPING**</span><span class="sxs-lookup"><span data-stu-id="e8e56-116">**PRJ_NOTIFICATION_MAPPING**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) | <span data-ttu-id="e8e56-117">描述通知對應，也就是目錄 (稱為「通知根目錄」 ) 和一組通知（以位遮罩表示）之間的配對。</span><span class="sxs-lookup"><span data-stu-id="e8e56-117">Describes a notification mapping, which is a pairing between a directory (referred to as a "notification root") and a set of notifications, expressed as a bit mask.</span></span> |
| [<span data-ttu-id="e8e56-118">**PRJ_NOTIFICATION_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="e8e56-118">**PRJ_NOTIFICATION_PARAMETERS**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_notification_parameters) | <span data-ttu-id="e8e56-119">通知的額外參數。</span><span class="sxs-lookup"><span data-stu-id="e8e56-119">Extra parameters for notifications.</span></span> |
| [<span data-ttu-id="e8e56-120">**PRJ_PLACEHOLDER_INFO**</span><span class="sxs-lookup"><span data-stu-id="e8e56-120">**PRJ_PLACEHOLDER_INFO**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) | <span data-ttu-id="e8e56-121">預留位置檔案或目錄的元資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e8e56-121">A buffer of metadata for the placeholder file or directory.</span></span> |
| [<span data-ttu-id="e8e56-122">**PRJ_PLACEHOLDER_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="e8e56-122">**PRJ_PLACEHOLDER_VERSION_INFO**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) | <span data-ttu-id="e8e56-123">可唯一識別預留位置檔案內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="e8e56-123">Information that uniquely identifies the contents of a placeholder file.</span></span> |
| [<span data-ttu-id="e8e56-124">**PRJ_STARTVIRTUALIZING_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="e8e56-124">**PRJ_STARTVIRTUALIZING_OPTIONS**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_startvirtualizing_options) | <span data-ttu-id="e8e56-125">啟動虛擬化實例時要提供的選項。</span><span class="sxs-lookup"><span data-stu-id="e8e56-125">Options to provide when starting a virtualization instance.</span></span> |
| [<span data-ttu-id="e8e56-126">**PRJ_VIRTUALIZATION_INSTANCE_INFO**</span><span class="sxs-lookup"><span data-stu-id="e8e56-126">**PRJ_VIRTUALIZATION_INSTANCE_INFO**</span></span>](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_virtualization_instance_info) | <span data-ttu-id="e8e56-127">虛擬化實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8e56-127">Information about a virtualization instance.</span></span> |
