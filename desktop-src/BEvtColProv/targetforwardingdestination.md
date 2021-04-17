---
description: 包含所收集資料的已知目的地。 只有在收集器在啟用狀態記錄檔的情況下才可使用。
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: TargetForwardingDestination 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467984"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="4b1a4-104">TargetForwardingDestination 類別</span><span class="sxs-lookup"><span data-stu-id="4b1a4-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="4b1a4-105">包含所收集資料的已知目的地。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="4b1a4-106">只有在收集器在啟用狀態記錄檔的情況下才可使用。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="4b1a4-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b1a4-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b1a4-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

## <a name="members"></a><span data-ttu-id="4b1a4-109">成員</span><span class="sxs-lookup"><span data-stu-id="4b1a4-109">Members</span></span>

<span data-ttu-id="4b1a4-110">**TargetForwardingDestination** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4b1a4-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="4b1a4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4b1a4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b1a4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4b1a4-112">Properties</span></span>

<span data-ttu-id="4b1a4-113">**TargetForwardingDestination** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b1a4-114">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-117">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-118">主機：收集端上端點的埠資訊。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-119">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-122">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-123">依收集器根據其設定決定的目標電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-125">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-127">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-128">建立連接的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-129">**目的地**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-133">資料的目的地。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-133">Destination of the data.</span></span> <span data-ttu-id="4b1a4-134">意義取決於轉寄站類型。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="4b1a4-135">可以是檔案名或其他識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-136">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-139">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-140">用來產生資料目的地的模式。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="4b1a4-141">意義取決於轉寄站類型和設定。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="4b1a4-142">若為固定目的地，就會與目的地本身相同。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="4b1a4-143">如果目的地的檔案有旋轉，則會包含將取代為目的地中實際索引的模式字元。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-144">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-145">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-147">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-148">中斷連接時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-149">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-152">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-153">如果發生錯誤，則為錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-153">Error message if an error was encountered.</span></span> <span data-ttu-id="4b1a4-154">否則將會是空的。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-155">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-158">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-159">轉寄站的類型 (例如 ' etl ' ) 。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-160">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-163">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-164">目的電腦的端點資訊，以人類看得懂的格式。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="4b1a4-165">這個屬性會格式化為 *主機*：*埠* 字串。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="4b1a4-166">例如，"127.0.0.1： 50000"。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-167">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-170">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-171">目的電腦的 SMBIOS GUID (已知的) 。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-172">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-175">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-176">目的電腦的 MAC 位址 (已知的) 。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="4b1a4-177">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b1a4-178">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="4b1a4-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4b1a4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b1a4-180">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b1a4-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b1a4-181">記錄此狀態變更的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4b1a4-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b1a4-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b1a4-182">Requirements</span></span>



| <span data-ttu-id="4b1a4-183">需求</span><span class="sxs-lookup"><span data-stu-id="4b1a4-183">Requirement</span></span> | <span data-ttu-id="4b1a4-184">值</span><span class="sxs-lookup"><span data-stu-id="4b1a4-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1a4-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b1a4-185">Minimum supported client</span></span><br/> | <span data-ttu-id="4b1a4-186">都不支援</span><span class="sxs-lookup"><span data-stu-id="4b1a4-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4b1a4-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b1a4-187">Minimum supported server</span></span><br/> | <span data-ttu-id="4b1a4-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4b1a4-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="4b1a4-189">命名空間</span><span class="sxs-lookup"><span data-stu-id="4b1a4-189">Namespace</span></span><br/>                | <span data-ttu-id="4b1a4-190">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="4b1a4-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="4b1a4-191">MOF</span><span class="sxs-lookup"><span data-stu-id="4b1a4-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b1a4-192"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b1a4-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b1a4-193">DLL</span><span class="sxs-lookup"><span data-stu-id="4b1a4-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b1a4-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b1a4-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

