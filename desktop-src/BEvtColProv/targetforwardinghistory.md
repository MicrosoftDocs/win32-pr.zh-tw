---
description: 目的電腦轉送資料變更的最近歷程記錄。
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: TargetForwardingHistory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111656"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="e6d85-103">TargetForwardingHistory 類別</span><span class="sxs-lookup"><span data-stu-id="e6d85-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="e6d85-104">目的電腦轉送資料變更的最近歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="e6d85-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="e6d85-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e6d85-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d85-106">語法</span><span class="sxs-lookup"><span data-stu-id="e6d85-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="e6d85-107">成員</span><span class="sxs-lookup"><span data-stu-id="e6d85-107">Members</span></span>

<span data-ttu-id="e6d85-108">**TargetForwardingHistory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e6d85-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="e6d85-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e6d85-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6d85-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e6d85-110">Properties</span></span>

<span data-ttu-id="e6d85-111">**TargetForwardingHistory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e6d85-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6d85-112">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e6d85-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-115">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-116">收集器伺服器的端點資訊。</span><span class="sxs-lookup"><span data-stu-id="e6d85-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="e6d85-117">這個屬性會格式化為 *主機*：*埠* 字串。</span><span class="sxs-lookup"><span data-stu-id="e6d85-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-118">**電腦**</span><span class="sxs-lookup"><span data-stu-id="e6d85-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-121">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-122">目的電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="e6d85-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-123">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="e6d85-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-124">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="e6d85-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-126">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-127">時間戳記，指出為轉送資料建立連接的時間。</span><span class="sxs-lookup"><span data-stu-id="e6d85-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-128">**目的地**</span><span class="sxs-lookup"><span data-stu-id="e6d85-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-131">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-132">轉送資料的目的地，例如檔案名。</span><span class="sxs-lookup"><span data-stu-id="e6d85-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-133">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="e6d85-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-136">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-137">用來產生轉送資料目的地的格式。</span><span class="sxs-lookup"><span data-stu-id="e6d85-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-138">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="e6d85-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-139">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="e6d85-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-141">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-142">指出連接中斷連接的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e6d85-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-143">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="e6d85-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-146">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-147">描述發生錯誤的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e6d85-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="e6d85-148">如果未發生任何錯誤，此屬性是空的。</span><span class="sxs-lookup"><span data-stu-id="e6d85-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-149">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="e6d85-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-152">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-153">包含轉送資料（例如 ETL）的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="e6d85-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-154">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e6d85-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-157">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-158">目的電腦的端點資訊，以人類看得懂的格式。</span><span class="sxs-lookup"><span data-stu-id="e6d85-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="e6d85-159">這個屬性會格式化為 *主機*：*埠* 字串。</span><span class="sxs-lookup"><span data-stu-id="e6d85-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="e6d85-160">例如，"127.0.0.1： 50000"。</span><span class="sxs-lookup"><span data-stu-id="e6d85-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-161">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="e6d85-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-164">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-165">目的電腦的 SMBIOS **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="e6d85-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-166">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="e6d85-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e6d85-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-169">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-170">目的電腦的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="e6d85-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6d85-171">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="e6d85-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d85-172">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="e6d85-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d85-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d85-174">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d85-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d85-175">記錄此狀態變更的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e6d85-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6d85-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6d85-176">Requirements</span></span>



| <span data-ttu-id="e6d85-177">需求</span><span class="sxs-lookup"><span data-stu-id="e6d85-177">Requirement</span></span> | <span data-ttu-id="e6d85-178">值</span><span class="sxs-lookup"><span data-stu-id="e6d85-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d85-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6d85-179">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d85-180">都不支援</span><span class="sxs-lookup"><span data-stu-id="e6d85-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e6d85-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6d85-181">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d85-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e6d85-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="e6d85-183">命名空間</span><span class="sxs-lookup"><span data-stu-id="e6d85-183">Namespace</span></span><br/>                | <span data-ttu-id="e6d85-184">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="e6d85-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="e6d85-185">MOF</span><span class="sxs-lookup"><span data-stu-id="e6d85-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6d85-186"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6d85-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6d85-187">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d85-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6d85-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6d85-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e6d85-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6d85-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d85-190">開機事件收集器 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="e6d85-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

