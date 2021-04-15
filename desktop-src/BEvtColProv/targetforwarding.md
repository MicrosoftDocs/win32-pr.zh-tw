---
description: 從目的電腦抓取轉送資料。
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: TargetForwarding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510388"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="2bce6-103">TargetForwarding 類別</span><span class="sxs-lookup"><span data-stu-id="2bce6-103">TargetForwarding class</span></span>

<span data-ttu-id="2bce6-104">從目的電腦抓取轉送資料。</span><span class="sxs-lookup"><span data-stu-id="2bce6-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="2bce6-105">目的電腦可以設定多個轉寄站。</span><span class="sxs-lookup"><span data-stu-id="2bce6-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="2bce6-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2bce6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bce6-107">語法</span><span class="sxs-lookup"><span data-stu-id="2bce6-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a><span data-ttu-id="2bce6-108">成員</span><span class="sxs-lookup"><span data-stu-id="2bce6-108">Members</span></span>

<span data-ttu-id="2bce6-109">**TargetForwarding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2bce6-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="2bce6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2bce6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bce6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2bce6-111">Properties</span></span>

<span data-ttu-id="2bce6-112">**TargetForwarding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2bce6-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bce6-113">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="2bce6-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-116">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-117">收集器伺服器的端點資訊。</span><span class="sxs-lookup"><span data-stu-id="2bce6-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="2bce6-118">這個屬性會格式化為 *主機*：*埠* 字串。</span><span class="sxs-lookup"><span data-stu-id="2bce6-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-119">**電腦**</span><span class="sxs-lookup"><span data-stu-id="2bce6-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-122">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-123">目的電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="2bce6-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="2bce6-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-125">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="2bce6-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-127">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-128">時間戳記，指出為轉送資料建立連接的時間。</span><span class="sxs-lookup"><span data-stu-id="2bce6-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-129">**目的地**</span><span class="sxs-lookup"><span data-stu-id="2bce6-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-132">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-133">轉送資料的目的地，例如檔案名。</span><span class="sxs-lookup"><span data-stu-id="2bce6-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-134">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="2bce6-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-137">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-138">用來產生轉送資料目的地的格式。</span><span class="sxs-lookup"><span data-stu-id="2bce6-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-139">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="2bce6-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-142">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-143">描述發生錯誤的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2bce6-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="2bce6-144">如果未發生任何錯誤，此屬性是空的。</span><span class="sxs-lookup"><span data-stu-id="2bce6-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-145">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="2bce6-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-148">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-149">包含轉送資料（例如 ETL）的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="2bce6-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-150">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="2bce6-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-153">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-154">目的電腦的端點資訊，以人類看得懂的格式。</span><span class="sxs-lookup"><span data-stu-id="2bce6-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="2bce6-155">這個屬性會格式化為 *主機*：*埠* 字串。</span><span class="sxs-lookup"><span data-stu-id="2bce6-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="2bce6-156">例如，"127.0.0.1： 50000"。</span><span class="sxs-lookup"><span data-stu-id="2bce6-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-157">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="2bce6-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-160">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-161">目的電腦的 SMBIOS **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="2bce6-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="2bce6-162">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="2bce6-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bce6-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bce6-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bce6-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bce6-165">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bce6-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bce6-166">目的電腦的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="2bce6-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bce6-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bce6-167">Requirements</span></span>



| <span data-ttu-id="2bce6-168">需求</span><span class="sxs-lookup"><span data-stu-id="2bce6-168">Requirement</span></span> | <span data-ttu-id="2bce6-169">值</span><span class="sxs-lookup"><span data-stu-id="2bce6-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bce6-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bce6-170">Minimum supported client</span></span><br/> | <span data-ttu-id="2bce6-171">都不支援</span><span class="sxs-lookup"><span data-stu-id="2bce6-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2bce6-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bce6-172">Minimum supported server</span></span><br/> | <span data-ttu-id="2bce6-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2bce6-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="2bce6-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="2bce6-174">Namespace</span></span><br/>                | <span data-ttu-id="2bce6-175">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="2bce6-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="2bce6-176">MOF</span><span class="sxs-lookup"><span data-stu-id="2bce6-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bce6-177"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bce6-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bce6-178">DLL</span><span class="sxs-lookup"><span data-stu-id="2bce6-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bce6-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2bce6-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2bce6-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bce6-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bce6-181">開機事件收集器 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="2bce6-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

