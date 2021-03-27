---
description: HWConfig 類別是 Windows XP 上硬體設定事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: HWConfig 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852803"
---
# <a name="hwconfig-class"></a><span data-ttu-id="3f9fa-104">HWConfig 類別</span><span class="sxs-lookup"><span data-stu-id="3f9fa-104">HWConfig class</span></span>

<span data-ttu-id="3f9fa-105">**HWConfig** 類別是 Windows XP 上硬體設定事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="3f9fa-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f9fa-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f9fa-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3f9fa-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f9fa-108">Members</span></span>

<span data-ttu-id="3f9fa-109">**HWConfig** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f9fa-110">備註</span><span class="sxs-lookup"><span data-stu-id="3f9fa-110">Remarks</span></span>

<span data-ttu-id="3f9fa-111">這些事件會提供電腦的硬體設定。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="3f9fa-112">不同于其他 NT 核心記錄器事件，核心會話會自動產生硬體設定事件;當您啟動 NT Kernel 記錄器會話時，不會啟用這些事件。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="3f9fa-113">**Windows 2000：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="3f9fa-114">如需 Windows Vista 和 Windows Server 2003 上的硬體設定事件，請參閱 [SystemConfig](systemconfig.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="3f9fa-115">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來執行硬體設定事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3f9fa-116">使用下列事件種類來識別使用事件時的實際硬體設定事件。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="3f9fa-117">事件類型</span><span class="sxs-lookup"><span data-stu-id="3f9fa-117">Event type</span></span>                                                                      | <span data-ttu-id="3f9fa-118">描述</span><span class="sxs-lookup"><span data-stu-id="3f9fa-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9fa-119">**活動 \_追蹤 \_ 類型 \_ 設定 \_ CPU** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="3f9fa-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="3f9fa-120">CPU 設定事件。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-120">CPU configuration event.</span></span> <span data-ttu-id="3f9fa-121">[**HWConfig \_ CPU**](hwconfig-cpu.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="3f9fa-122">**活動 \_追蹤 \_ 類型 \_ 設定 \_ LOGICALDISK** (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="3f9fa-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="3f9fa-123">邏輯磁片設定事件。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-123">Logical disk configuration event.</span></span> <span data-ttu-id="3f9fa-124">[**HWConfig \_ LogDisk**](hwconfig-logdisk.md) mof 類別 mof 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3f9fa-125">**活動 \_追蹤 \_ 類型 \_ CONFIG \_ NIC** (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="3f9fa-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="3f9fa-126">NIC 設定事件。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-126">NIC configuration event.</span></span> <span data-ttu-id="3f9fa-127">[**HWConfig \_ NIC**](hwconfig-nic.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="3f9fa-128">**活動 \_追蹤 \_ 類型 \_ 設定 \_ PHYSICALDISK** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="3f9fa-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="3f9fa-129">實體磁片設定事件。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-129">Physical disk configuration event.</span></span> <span data-ttu-id="3f9fa-130">[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3f9fa-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="3f9fa-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f9fa-131">Requirements</span></span>



| <span data-ttu-id="3f9fa-132">需求</span><span class="sxs-lookup"><span data-stu-id="3f9fa-132">Requirement</span></span> | <span data-ttu-id="3f9fa-133">值</span><span class="sxs-lookup"><span data-stu-id="3f9fa-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="3f9fa-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f9fa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3f9fa-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f9fa-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3f9fa-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f9fa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3f9fa-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="3f9fa-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="3f9fa-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f9fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f9fa-139">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="3f9fa-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="3f9fa-140">**HWConfig \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="3f9fa-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="3f9fa-141">**HWConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="3f9fa-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="3f9fa-142">**HWConfig \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="3f9fa-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="3f9fa-143">**HWConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="3f9fa-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 
