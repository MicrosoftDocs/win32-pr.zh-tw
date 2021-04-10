---
title: TaskSettings. NetworkSettings 屬性
description: 針對腳本，取得或設定包含網路設定檔識別碼和名稱的網路設定物件。
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- NetworkSettings 屬性工作排程器
- NetworkSettings 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、NetworkSettings 屬性
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685639"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="6e2ff-106">TaskSettings. NetworkSettings 屬性</span><span class="sxs-lookup"><span data-stu-id="6e2ff-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="6e2ff-107">針對腳本，取得或設定包含網路設定檔識別碼和名稱的網路設定物件。</span><span class="sxs-lookup"><span data-stu-id="6e2ff-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="6e2ff-108">如果 [**TaskSettings**](tasksettings.md)的 [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)屬性為 **True** ，而且 **NetworkSettings** 屬性中指定了網路 propfile，則只有在指定的網路設定檔可用時，才會執行此工作。</span><span class="sxs-lookup"><span data-stu-id="6e2ff-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e2ff-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e2ff-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="6e2ff-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6e2ff-110">Property value</span></span>

<span data-ttu-id="6e2ff-111">[**NetworkSettings**](networksettings.md)物件，其中包含網路設定檔識別碼和名稱。</span><span class="sxs-lookup"><span data-stu-id="6e2ff-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e2ff-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e2ff-112">Requirements</span></span>



| <span data-ttu-id="6e2ff-113">需求</span><span class="sxs-lookup"><span data-stu-id="6e2ff-113">Requirement</span></span> | <span data-ttu-id="6e2ff-114">值</span><span class="sxs-lookup"><span data-stu-id="6e2ff-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2ff-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e2ff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6e2ff-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e2ff-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6e2ff-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e2ff-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6e2ff-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e2ff-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e2ff-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6e2ff-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e2ff-120"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6e2ff-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6e2ff-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6e2ff-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e2ff-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e2ff-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e2ff-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e2ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e2ff-124">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="6e2ff-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="6e2ff-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="6e2ff-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





