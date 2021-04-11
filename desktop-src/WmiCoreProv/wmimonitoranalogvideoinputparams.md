---
description: 代表電腦監視器的類比影片輸入參數。
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: WmiMonitorAnalogVideoInputParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944596"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="6091c-103">WmiMonitorAnalogVideoInputParams 類別</span><span class="sxs-lookup"><span data-stu-id="6091c-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="6091c-104">**WmiMonitorAnalogVideoInputParams** WMI 類別代表電腦監視器的類比影片輸入參數。</span><span class="sxs-lookup"><span data-stu-id="6091c-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="6091c-105">此類別中的資料會對應至視頻電子郵件標準關聯的影片輸入定義中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。</span><span class="sxs-lookup"><span data-stu-id="6091c-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="6091c-106">只有當 [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)類別的 **VideoInputType** 屬性值為 "類比" 時，才能使用這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6091c-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="6091c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6091c-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="6091c-108">成員</span><span class="sxs-lookup"><span data-stu-id="6091c-108">Members</span></span>

<span data-ttu-id="6091c-109">**WmiMonitorAnalogVideoInputParams** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6091c-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="6091c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6091c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6091c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6091c-111">Properties</span></span>

<span data-ttu-id="6091c-112">**WmiMonitorAnalogVideoInputParams** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6091c-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6091c-113">**使用中**</span><span class="sxs-lookup"><span data-stu-id="6091c-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-114">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6091c-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-116">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="6091c-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6091c-117">**CompositeSyncSupported**</span><span class="sxs-lookup"><span data-stu-id="6091c-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-118">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6091c-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-120">指出是否支援複合同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="6091c-121">值</span><span class="sxs-lookup"><span data-stu-id="6091c-121">Value</span></span>                                                                              | <span data-ttu-id="6091c-122">意義</span><span class="sxs-lookup"><span data-stu-id="6091c-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="6091c-123"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6091c-124">支援水準同步處理線上的複合同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="6091c-125"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6091c-126">不支援水準同步處理行上的複合同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6091c-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="6091c-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6091c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6091c-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="6091c-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6091c-131">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="6091c-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="6091c-132">**SeparateSyncsSupported**</span><span class="sxs-lookup"><span data-stu-id="6091c-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-133">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6091c-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-135">指出是否支援個別同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="6091c-136">值</span><span class="sxs-lookup"><span data-stu-id="6091c-136">Value</span></span>                                                                              | <span data-ttu-id="6091c-137">意義</span><span class="sxs-lookup"><span data-stu-id="6091c-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6091c-138"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6091c-139">支援不同的同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="6091c-140"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6091c-141">不支援個別的同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6091c-142">**SerrationOfVsyncRequired**</span><span class="sxs-lookup"><span data-stu-id="6091c-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-143">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6091c-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-145">指出是否需要垂直同步脈衝 serration。</span><span class="sxs-lookup"><span data-stu-id="6091c-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="6091c-146">值</span><span class="sxs-lookup"><span data-stu-id="6091c-146">Value</span></span>                                                                              | <span data-ttu-id="6091c-147">意義</span><span class="sxs-lookup"><span data-stu-id="6091c-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6091c-148"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6091c-149">使用複合同步處理或同步處理-綠色影片時，需要垂直同步脈衝的 Serration。</span><span class="sxs-lookup"><span data-stu-id="6091c-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="6091c-150"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6091c-151">使用複合同步處理或「同步-開啟」影片時，不需要 Serration 垂直同步脈衝。</span><span class="sxs-lookup"><span data-stu-id="6091c-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6091c-152">**SetupExpected**</span><span class="sxs-lookup"><span data-stu-id="6091c-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-153">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6091c-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-155">指出是否預期安裝程式。</span><span class="sxs-lookup"><span data-stu-id="6091c-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="6091c-156">值</span><span class="sxs-lookup"><span data-stu-id="6091c-156">Value</span></span>                                                                              | <span data-ttu-id="6091c-157">意義</span><span class="sxs-lookup"><span data-stu-id="6091c-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6091c-158"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6091c-159">監視器預期每個適當的信號等級標準會有空白到空白的設定或基座。</span><span class="sxs-lookup"><span data-stu-id="6091c-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="6091c-160"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6091c-161">根據適當的信號等級標準，監視不會預期會有空白到空白的設定或基座。</span><span class="sxs-lookup"><span data-stu-id="6091c-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6091c-162">**SignalLevelStandard**</span><span class="sxs-lookup"><span data-stu-id="6091c-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-163">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6091c-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-165">增強型視頻連接器的信號等級標準 (的 EVC) 連接。</span><span class="sxs-lookup"><span data-stu-id="6091c-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="6091c-166">值</span><span class="sxs-lookup"><span data-stu-id="6091c-166">Value</span></span>                                                                              | <span data-ttu-id="6091c-167">意義</span><span class="sxs-lookup"><span data-stu-id="6091c-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="6091c-168"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6091c-169">0.7，0.3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6091c-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="6091c-170"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6091c-171">0.714，0.286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6091c-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="6091c-172"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="6091c-173">1.0、0.4 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6091c-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="6091c-174"><dt>3 (0x3) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="6091c-175">0.7、0.0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6091c-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="6091c-176">**SyncOnGreenVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="6091c-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6091c-177">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6091c-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6091c-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6091c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6091c-179">指出是否支援在綠色上進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="6091c-180">值</span><span class="sxs-lookup"><span data-stu-id="6091c-180">Value</span></span>                                                                              | <span data-ttu-id="6091c-181">意義</span><span class="sxs-lookup"><span data-stu-id="6091c-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6091c-182"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6091c-183">支援在綠色影片上進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="6091c-184"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="6091c-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6091c-185">不支援在綠色影片上進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="6091c-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6091c-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="6091c-186">Requirements</span></span>



| <span data-ttu-id="6091c-187">需求</span><span class="sxs-lookup"><span data-stu-id="6091c-187">Requirement</span></span> | <span data-ttu-id="6091c-188">值</span><span class="sxs-lookup"><span data-stu-id="6091c-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6091c-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6091c-189">Minimum supported client</span></span><br/> | <span data-ttu-id="6091c-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6091c-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6091c-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6091c-191">Minimum supported server</span></span><br/> | <span data-ttu-id="6091c-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6091c-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6091c-193">命名空間</span><span class="sxs-lookup"><span data-stu-id="6091c-193">Namespace</span></span><br/>                | <span data-ttu-id="6091c-194">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="6091c-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6091c-195">MOF</span><span class="sxs-lookup"><span data-stu-id="6091c-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6091c-196"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="6091c-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6091c-197">DLL</span><span class="sxs-lookup"><span data-stu-id="6091c-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6091c-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6091c-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6091c-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6091c-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6091c-200">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="6091c-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




