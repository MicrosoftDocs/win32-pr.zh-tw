---
description: 代表受支援的監視器顯示功能。
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978836"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="1ba54-103">SupportedDisplayFeaturesDescriptor 類別</span><span class="sxs-lookup"><span data-stu-id="1ba54-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="1ba54-104">**SupportedDisplayFeaturesDescriptor** 代表受支援的監視器顯示功能。</span><span class="sxs-lookup"><span data-stu-id="1ba54-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="1ba54-105">此類別中的資訊會對應至視頻電子產品標準關聯的影片輸入定義中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。</span><span class="sxs-lookup"><span data-stu-id="1ba54-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba54-106">語法</span><span class="sxs-lookup"><span data-stu-id="1ba54-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="1ba54-107">成員</span><span class="sxs-lookup"><span data-stu-id="1ba54-107">Members</span></span>

<span data-ttu-id="1ba54-108">**SupportedDisplayFeaturesDescriptor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ba54-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="1ba54-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1ba54-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ba54-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1ba54-110">Properties</span></span>

<span data-ttu-id="1ba54-111">**SupportedDisplayFeaturesDescriptor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ba54-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ba54-112">**ActiveOffSupported**</span><span class="sxs-lookup"><span data-stu-id="1ba54-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ba54-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-115">支援主動式電源和非常低的耗電量。</span><span class="sxs-lookup"><span data-stu-id="1ba54-115">Support for active off and very low power.</span></span> <span data-ttu-id="1ba54-116">當顯示器收到的計時信號超出宣告的作用中作業範圍時，就會耗用較少的電源。</span><span class="sxs-lookup"><span data-stu-id="1ba54-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="1ba54-117">如果計時信號回到正常的作業範圍，則顯示會還原為一般作業。</span><span class="sxs-lookup"><span data-stu-id="1ba54-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="1ba54-118">一般作業範圍外的計時信號範例不是任何同步信號，也不會有任何取消信號。</span><span class="sxs-lookup"><span data-stu-id="1ba54-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="1ba54-119">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="1ba54-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-120">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1ba54-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-122">監視器的顯示類型。</span><span class="sxs-lookup"><span data-stu-id="1ba54-122">Type of display for the monitor.</span></span> <span data-ttu-id="1ba54-123">下表列出可能的值。</span><span class="sxs-lookup"><span data-stu-id="1ba54-123">The following table lists possible values.</span></span>



| <span data-ttu-id="1ba54-124">值</span><span class="sxs-lookup"><span data-stu-id="1ba54-124">Value</span></span>                                                                              | <span data-ttu-id="1ba54-125">意義</span><span class="sxs-lookup"><span data-stu-id="1ba54-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="1ba54-126"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="1ba54-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="1ba54-127">單色/灰階顯示</span><span class="sxs-lookup"><span data-stu-id="1ba54-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="1ba54-128"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="1ba54-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="1ba54-129">RGB 色彩顯示</span><span class="sxs-lookup"><span data-stu-id="1ba54-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="1ba54-130"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="1ba54-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="1ba54-131">非 RGB 多色顯示</span><span class="sxs-lookup"><span data-stu-id="1ba54-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="1ba54-132">**GTFSupported**</span><span class="sxs-lookup"><span data-stu-id="1ba54-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ba54-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-135">指出顯示器是否具有 GTF 支援。</span><span class="sxs-lookup"><span data-stu-id="1ba54-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="1ba54-136">若 **為 True**，則顯示使用預設 GTF 參數值，以 GTF 標準為基礎來支援計時。</span><span class="sxs-lookup"><span data-stu-id="1ba54-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="1ba54-137">**HasPreferredTimingMode**</span><span class="sxs-lookup"><span data-stu-id="1ba54-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ba54-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-140">指出顯示器是否有慣用的時間模式。</span><span class="sxs-lookup"><span data-stu-id="1ba54-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="1ba54-141">若 **為 True**，則第一個詳細計時區塊包含監視的慣用計時模式。</span><span class="sxs-lookup"><span data-stu-id="1ba54-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="1ba54-142">使用慣用的時間模式是 EDID v1.0 和更新版本的必要項。</span><span class="sxs-lookup"><span data-stu-id="1ba54-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="1ba54-143">**sRGBSupported**</span><span class="sxs-lookup"><span data-stu-id="1ba54-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ba54-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-146">若 **為 True**，則顯示支援 sRGB。</span><span class="sxs-lookup"><span data-stu-id="1ba54-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="1ba54-147">**StandbySupported**</span><span class="sxs-lookup"><span data-stu-id="1ba54-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ba54-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-150">指出顯示器是否支援 VESA 顯示器電源管理信號 (DPMS) 待命。</span><span class="sxs-lookup"><span data-stu-id="1ba54-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="1ba54-151">若 **為 True**，則支援 DPMS 待命。</span><span class="sxs-lookup"><span data-stu-id="1ba54-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="1ba54-152">**SuspendSupported**</span><span class="sxs-lookup"><span data-stu-id="1ba54-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba54-153">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ba54-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba54-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba54-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba54-155">指出顯示器是否支援 VESA 顯示器電源管理信號 (DPMS) 暫停。</span><span class="sxs-lookup"><span data-stu-id="1ba54-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="1ba54-156">若 **為 True**，則支援 DPMS 暫止。</span><span class="sxs-lookup"><span data-stu-id="1ba54-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ba54-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ba54-157">Requirements</span></span>



| <span data-ttu-id="1ba54-158">需求</span><span class="sxs-lookup"><span data-stu-id="1ba54-158">Requirement</span></span> | <span data-ttu-id="1ba54-159">值</span><span class="sxs-lookup"><span data-stu-id="1ba54-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba54-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ba54-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba54-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ba54-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1ba54-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ba54-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba54-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ba54-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1ba54-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="1ba54-164">Namespace</span></span><br/>                | <span data-ttu-id="1ba54-165">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="1ba54-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1ba54-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1ba54-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ba54-167"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ba54-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ba54-168">DLL</span><span class="sxs-lookup"><span data-stu-id="1ba54-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ba54-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ba54-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba54-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ba54-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba54-171">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1ba54-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




