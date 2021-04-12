---
title: NetworkSettings 物件
description: 針對腳本，提供工作排程器服務用來取得網路設定檔的設定。
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- NetworkSettings 物件工作排程器
- NetworkSettings 物件工作排程器，說明
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465632"
---
# <a name="networksettings-object"></a><span data-ttu-id="ba182-105">NetworkSettings 物件</span><span class="sxs-lookup"><span data-stu-id="ba182-105">NetworkSettings object</span></span>

<span data-ttu-id="ba182-106">針對腳本，提供工作排程器服務用來取得網路設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="ba182-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="ba182-107">成員</span><span class="sxs-lookup"><span data-stu-id="ba182-107">Members</span></span>

<span data-ttu-id="ba182-108">**NetworkSettings** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ba182-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="ba182-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ba182-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba182-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ba182-110">Properties</span></span>

<span data-ttu-id="ba182-111">**NetworkSettings** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ba182-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="ba182-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ba182-112">Property</span></span>                                        | <span data-ttu-id="ba182-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="ba182-113">Access type</span></span>           | <span data-ttu-id="ba182-114">Description</span><span class="sxs-lookup"><span data-stu-id="ba182-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba182-115">**Id**</span><span class="sxs-lookup"><span data-stu-id="ba182-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="ba182-116">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba182-116">Read/write</span></span><br/> | <span data-ttu-id="ba182-117">取得或設定可識別網路設定檔的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="ba182-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="ba182-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="ba182-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="ba182-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba182-119">Read/write</span></span><br/> | <span data-ttu-id="ba182-120">取得或設定網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba182-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="ba182-121">此名稱會用於顯示用途。</span><span class="sxs-lookup"><span data-stu-id="ba182-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba182-122">備註</span><span class="sxs-lookup"><span data-stu-id="ba182-122">Remarks</span></span>

<span data-ttu-id="ba182-123">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) 元素來指定網路設定。</span><span class="sxs-lookup"><span data-stu-id="ba182-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba182-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba182-124">Requirements</span></span>



| <span data-ttu-id="ba182-125">需求</span><span class="sxs-lookup"><span data-stu-id="ba182-125">Requirement</span></span> | <span data-ttu-id="ba182-126">值</span><span class="sxs-lookup"><span data-stu-id="ba182-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba182-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba182-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ba182-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba182-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ba182-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba182-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ba182-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba182-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba182-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ba182-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba182-132"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ba182-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ba182-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ba182-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba182-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba182-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba182-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba182-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba182-136">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="ba182-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="ba182-137">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ba182-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





