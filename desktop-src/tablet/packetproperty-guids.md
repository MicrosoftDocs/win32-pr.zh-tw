---
description: 下表列出封包屬性結構所使用的封包屬性 Guid \_ 。
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852812"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="6a08a-103">PacketProperty Guid</span><span class="sxs-lookup"><span data-stu-id="6a08a-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="6a08a-104">下表列出封 [**包 \_ 屬性**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) 結構所使用的封包屬性 guid。</span><span class="sxs-lookup"><span data-stu-id="6a08a-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a08a-105">GUID</span><span class="sxs-lookup"><span data-stu-id="6a08a-105">GUID</span></span></th>
<th><span data-ttu-id="6a08a-106">Description</span><span class="sxs-lookup"><span data-stu-id="6a08a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a08a-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="6a08a-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="6a08a-108">畫筆軸和平板電腦表面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="6a08a-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="6a08a-109">當畫筆平行至介面時，此值為0，當畫筆垂直至表面時，則為90。</span><span class="sxs-lookup"><span data-stu-id="6a08a-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="6a08a-110">當畫筆反轉時，值為負數。</span><span class="sxs-lookup"><span data-stu-id="6a08a-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="6a08a-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="6a08a-112">透過完整的圓形範圍，在 Z 軸上順時針旋轉游標。</span><span class="sxs-lookup"><span data-stu-id="6a08a-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="6a08a-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="6a08a-114">當辨識器以 box 模式操作時，用來取得筆跡辨識替代方塊的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6a08a-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="6a08a-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="6a08a-116">壓力相關按鈕的壓力。</span><span class="sxs-lookup"><span data-stu-id="6a08a-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="6a08a-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="6a08a-118">PacketProperty 物件的 GUID，表示與 tablet 介面垂直的鋼筆提示壓力。</span><span class="sxs-lookup"><span data-stu-id="6a08a-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="6a08a-119">畫筆秘訣的壓力愈大，繪製的筆墨越多。</span><span class="sxs-lookup"><span data-stu-id="6a08a-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="6a08a-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="6a08a-121">包含下列一或多個旗標值：</span><span class="sxs-lookup"><span data-stu-id="6a08a-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="6a08a-122">游標觸及繪圖介面 (Value = 1) 。</span><span class="sxs-lookup"><span data-stu-id="6a08a-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="6a08a-123">資料指標反轉。</span><span class="sxs-lookup"><span data-stu-id="6a08a-123">The cursor is inverted.</span></span> <span data-ttu-id="6a08a-124">例如，畫筆的橡皮擦末端指向介面 (值 = 2) 。</span><span class="sxs-lookup"><span data-stu-id="6a08a-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="6a08a-125">未使用 (值 = 4) 。</span><span class="sxs-lookup"><span data-stu-id="6a08a-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="6a08a-126">已按下 [圓筒] 按鈕 (值 = 8) 。</span><span class="sxs-lookup"><span data-stu-id="6a08a-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="6a08a-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="6a08a-128">封包的裝置連絡人識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a08a-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="6a08a-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="6a08a-130">識別封包。</span><span class="sxs-lookup"><span data-stu-id="6a08a-130">Identifies the packet.</span></span> <span data-ttu-id="6a08a-131">這是您用來從封包佇列取出封包的相同值。</span><span class="sxs-lookup"><span data-stu-id="6a08a-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="6a08a-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="6a08a-133">PacketProperty 物件的 GUID，這個物件表示沿著 tablet 介面平面之畫筆提示的壓力。</span><span class="sxs-lookup"><span data-stu-id="6a08a-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="6a08a-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="6a08a-135">產生封包的時間。</span><span class="sxs-lookup"><span data-stu-id="6a08a-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="6a08a-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="6a08a-137">以順時針旋轉其本身軸的游標。</span><span class="sxs-lookup"><span data-stu-id="6a08a-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="6a08a-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="6a08a-139">Tablet 座標空間中的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="6a08a-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="6a08a-140">依預設，每個封包都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6a08a-140">Each packet contains this property by default.</span></span> <span data-ttu-id="6a08a-141">平板電腦的原點 (0、0) 是左上角。</span><span class="sxs-lookup"><span data-stu-id="6a08a-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="6a08a-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="6a08a-143">若為畫筆游標，x 傾斜方向是 y、z 平面和畫筆和 y 軸平面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="6a08a-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="6a08a-144">當畫筆垂直至繪圖介面時，此值為0，而當畫筆位於垂直右方時為正數。</span><span class="sxs-lookup"><span data-stu-id="6a08a-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="6a08a-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="6a08a-146">Tablet 座標空間中的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="6a08a-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="6a08a-147">依預設，每個封包都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6a08a-147">Each packet contains this property by default.</span></span> <span data-ttu-id="6a08a-148">平板電腦的原點 (0、0) 是左上角。</span><span class="sxs-lookup"><span data-stu-id="6a08a-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a08a-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="6a08a-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="6a08a-150">若為畫筆游標，y 傾斜方向是 x、z 平面和畫筆和 X 軸平面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="6a08a-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="6a08a-151">當畫筆垂直至繪圖介面時，此值為0，當畫筆向上或遠離使用者時，此值為正數。</span><span class="sxs-lookup"><span data-stu-id="6a08a-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a08a-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="6a08a-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="6a08a-153">Tablet 介面中畫筆提示的 z 座標或距離。</span><span class="sxs-lookup"><span data-stu-id="6a08a-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="6a08a-154"><a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a>列舉型別會決定這個屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="6a08a-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="6a08a-155">TangentPressure 欄位代表 tablet 表面平面的壓力;NormalPressure 欄位代表與 tablet 表面平面垂直的壓力。</span><span class="sxs-lookup"><span data-stu-id="6a08a-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 




