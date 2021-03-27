---
description: 此類別是硬體設定事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: SystemConfig 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853172"
---
# <a name="systemconfig-class"></a><span data-ttu-id="c88e5-104">SystemConfig 類別</span><span class="sxs-lookup"><span data-stu-id="c88e5-104">SystemConfig class</span></span>

<span data-ttu-id="c88e5-105">此類別是硬體設定事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="c88e5-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="c88e5-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c88e5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88e5-107">語法</span><span class="sxs-lookup"><span data-stu-id="c88e5-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c88e5-108">成員</span><span class="sxs-lookup"><span data-stu-id="c88e5-108">Members</span></span>

<span data-ttu-id="c88e5-109">**SystemConfig** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="c88e5-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88e5-110">備註</span><span class="sxs-lookup"><span data-stu-id="c88e5-110">Remarks</span></span>

<span data-ttu-id="c88e5-111">這些事件會提供電腦的硬體設定。</span><span class="sxs-lookup"><span data-stu-id="c88e5-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="c88e5-112">不同于其他 NT 核心記錄器事件，核心會話會自動產生硬體設定事件;當您啟動 NT Kernel 記錄器會話時，不會啟用這些事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="c88e5-113">如需 Windows XP 上的硬體設定事件，請參閱 [HWConfig](hwconfig.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="c88e5-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="c88e5-114">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來執行硬體設定事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="c88e5-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c88e5-115">使用下列事件種類來識別使用事件時的實際硬體設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="c88e5-116">事件類型</span><span class="sxs-lookup"><span data-stu-id="c88e5-116">Event type</span></span>                                                                      | <span data-ttu-id="c88e5-117">描述</span><span class="sxs-lookup"><span data-stu-id="c88e5-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88e5-118">**活動 \_追蹤 \_ 類型 \_ 設定 \_ CPU** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="c88e5-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="c88e5-119">CPU 設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-119">CPU configuration event.</span></span> <span data-ttu-id="c88e5-120">[**SystemConfig \_ CPU**](systemconfig-cpu.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="c88e5-121">**活動 \_追蹤 \_ 類型 \_ 設定 \_ IDECHANNEL** (事件種類值為 23) </span><span class="sxs-lookup"><span data-stu-id="c88e5-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="c88e5-122">主要和次要 IDE 通道設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="c88e5-123">[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) mof 類別 mof 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c88e5-124">**活動 \_追蹤 \_ 類型 \_ 設定 \_ IRQ** (事件種類值為 21) </span><span class="sxs-lookup"><span data-stu-id="c88e5-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="c88e5-125">中斷要求 (IRQ) 事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="c88e5-126">[**SystemConfig \_ IRQ**](systemconfig-irq.md) mof 類別 mof 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="c88e5-127">**活動 \_追蹤 \_ 類型 \_ 設定 \_ LOGICALDISK** (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="c88e5-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="c88e5-128">邏輯磁片設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-128">Logical disk configuration event.</span></span> <span data-ttu-id="c88e5-129">[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) mof 類別 mof 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="c88e5-130">**活動 \_追蹤 \_ 類型 \_ 設定 \_ NETINFO** (事件種類值為 17) </span><span class="sxs-lookup"><span data-stu-id="c88e5-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="c88e5-131">網路 iformation 事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-131">Network iformation event.</span></span> <span data-ttu-id="c88e5-132">[**SystemConfig \_ Network**](systemconfig-network.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="c88e5-133">**活動 \_追蹤 \_ 類型 \_ CONFIG \_ NIC** (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="c88e5-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="c88e5-134">NIC 設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-134">NIC configuration event.</span></span> <span data-ttu-id="c88e5-135">[**SystemConfig \_ NIC**](systemconfig-nic.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="c88e5-136">**活動 \_追蹤 \_ 類型 \_ 設定 \_ PHYSICALDISK** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="c88e5-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="c88e5-137">實體磁片設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-137">Physical disk configuration event.</span></span> <span data-ttu-id="c88e5-138">[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="c88e5-139">**活動 \_追蹤 \_ 類型 \_ CONFIG \_ PNP** (事件種類值為 22) </span><span class="sxs-lookup"><span data-stu-id="c88e5-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="c88e5-140">隨插即用事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-140">Plug and play event.</span></span> <span data-ttu-id="c88e5-141">[**SystemConfig \_ PNP**](systemconfig-pnp.md) mof 類別 MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="c88e5-142">**活動 \_追蹤 \_ 類型 \_ CONFIG \_ POWER** (事件種類值為 16) </span><span class="sxs-lookup"><span data-stu-id="c88e5-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="c88e5-143">電源設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-143">Power configuration event.</span></span> <span data-ttu-id="c88e5-144">[**SystemConfig \_ 電源**](systemconfig-power.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="c88e5-145">**活動 \_追蹤 \_ 類型 \_ 設定 \_ 服務** (事件種類值為 15) </span><span class="sxs-lookup"><span data-stu-id="c88e5-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="c88e5-146">服務設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-146">Services configuration event.</span></span> <span data-ttu-id="c88e5-147">[**SystemConfig \_ Services**](systemconfig-services.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="c88e5-148">**活動 \_追蹤 \_ 類型 \_ 設定 \_ 影片** (事件種類值為 14) </span><span class="sxs-lookup"><span data-stu-id="c88e5-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="c88e5-149">圖形配接器設定事件。</span><span class="sxs-lookup"><span data-stu-id="c88e5-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="c88e5-150">[**SystemConfig \_ Video**](systemconfig-video.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="c88e5-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="c88e5-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="c88e5-151">Requirements</span></span>



| <span data-ttu-id="c88e5-152">需求</span><span class="sxs-lookup"><span data-stu-id="c88e5-152">Requirement</span></span> | <span data-ttu-id="c88e5-153">值</span><span class="sxs-lookup"><span data-stu-id="c88e5-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c88e5-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c88e5-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c88e5-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c88e5-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c88e5-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c88e5-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c88e5-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c88e5-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c88e5-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c88e5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88e5-159">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="c88e5-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="c88e5-160">**SystemConfig \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="c88e5-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="c88e5-161">**SystemConfig \_ IDEChannel**</span><span class="sxs-lookup"><span data-stu-id="c88e5-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="c88e5-162">**SystemConfig \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="c88e5-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="c88e5-163">**SystemConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="c88e5-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="c88e5-164">**SystemConfig \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="c88e5-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="c88e5-165">**SystemConfig \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="c88e5-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="c88e5-166">**SystemConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="c88e5-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="c88e5-167">**SystemConfig \_ PNP**</span><span class="sxs-lookup"><span data-stu-id="c88e5-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="c88e5-168">**SystemConfig \_ 電源**</span><span class="sxs-lookup"><span data-stu-id="c88e5-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="c88e5-169">**SystemConfig \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="c88e5-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="c88e5-170">**SystemConfig \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="c88e5-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="c88e5-171">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c88e5-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
