---
description: 代表 CRT 桌面監視器。
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: 'CIM_DesktopMonitor 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972683"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="b58d7-103">CIM_DesktopMonitor 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="b58d7-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="b58d7-104">代表 CRT 桌面監視器。</span><span class="sxs-lookup"><span data-stu-id="b58d7-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b58d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="b58d7-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="b58d7-106">成員</span><span class="sxs-lookup"><span data-stu-id="b58d7-106">Members</span></span>

<span data-ttu-id="b58d7-107">**CIM \_ DesktopMonitor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b58d7-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="b58d7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b58d7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b58d7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b58d7-109">Properties</span></span>

<span data-ttu-id="b58d7-110">**CIM \_ DesktopMonitor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b58d7-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b58d7-111">**頻寬**</span><span class="sxs-lookup"><span data-stu-id="b58d7-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58d7-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b58d7-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58d7-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b58d7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b58d7-114">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "mhz" ) ， **PUnit** ( "赫茲 \* 10 ^ 6" ) </span><span class="sxs-lookup"><span data-stu-id="b58d7-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="b58d7-115">MHertz 中顯示的頻寬。</span><span class="sxs-lookup"><span data-stu-id="b58d7-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="b58d7-116">"0" 表示不明。</span><span class="sxs-lookup"><span data-stu-id="b58d7-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b58d7-117">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="b58d7-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58d7-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b58d7-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b58d7-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b58d7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58d7-120">CRT 監視器的顯示類型類型。</span><span class="sxs-lookup"><span data-stu-id="b58d7-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="b58d7-121">例如，multiscan color 或單色。</span><span class="sxs-lookup"><span data-stu-id="b58d7-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b58d7-122">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b58d7-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b58d7-123">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b58d7-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="b58d7-124">**Multiscan 色彩** (2) </span><span class="sxs-lookup"><span data-stu-id="b58d7-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="b58d7-125">**Multiscan 單色** (3) </span><span class="sxs-lookup"><span data-stu-id="b58d7-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="b58d7-126">**固定頻率色彩** (4) </span><span class="sxs-lookup"><span data-stu-id="b58d7-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="b58d7-127">**固定頻率單色** (5) </span><span class="sxs-lookup"><span data-stu-id="b58d7-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b58d7-128">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="b58d7-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58d7-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b58d7-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58d7-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b58d7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58d7-131">顯示器的邏輯高度，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="b58d7-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b58d7-132">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="b58d7-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58d7-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b58d7-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58d7-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b58d7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58d7-135">顯示器的邏輯寬度，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="b58d7-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b58d7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="b58d7-136">Requirements</span></span>



| <span data-ttu-id="b58d7-137">需求</span><span class="sxs-lookup"><span data-stu-id="b58d7-137">Requirement</span></span> | <span data-ttu-id="b58d7-138">值</span><span class="sxs-lookup"><span data-stu-id="b58d7-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58d7-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b58d7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b58d7-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b58d7-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b58d7-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b58d7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b58d7-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b58d7-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b58d7-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="b58d7-143">Namespace</span></span><br/>                | <span data-ttu-id="b58d7-144">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b58d7-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b58d7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="b58d7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b58d7-146"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b58d7-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b58d7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b58d7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b58d7-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b58d7-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b58d7-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b58d7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58d7-150">**CIM \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="b58d7-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

