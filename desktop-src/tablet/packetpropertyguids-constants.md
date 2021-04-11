---
description: 定義指定封包屬性的值。
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: 'PacketPropertyGuids 常數 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195103"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="c4e86-103">PacketPropertyGuids 常數</span><span class="sxs-lookup"><span data-stu-id="c4e86-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="c4e86-104">定義指定封包屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c4e86-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="c4e86-105">Tablet PCAPI 會使用全域唯一識別碼 (Guid) 來識別封包屬性（在 COM 中是常數位符串）。</span><span class="sxs-lookup"><span data-stu-id="c4e86-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="c4e86-106">在 c + + 中，您可以在 Msinkaut .h 標頭檔中存取這些常數， <systemdrive> \\ \\ \\ \\ \\ 如果您將 SDK 安裝在預設位置，該檔案位於： Program Files Microsoft sdk Windows 6.0 Include 目錄。</span><span class="sxs-lookup"><span data-stu-id="c4e86-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="c4e86-107">在 c + + 中，這些常數是 WCHARs，而不是 Bstr。</span><span class="sxs-lookup"><span data-stu-id="c4e86-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="c4e86-108">使用之前，請先將它們轉換成 Bstr。</span><span class="sxs-lookup"><span data-stu-id="c4e86-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="c4e86-109">如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="c4e86-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="c4e86-110">下表列出可用的封包屬性全域唯一識別碼 (GUID) 欄位。</span><span class="sxs-lookup"><span data-stu-id="c4e86-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="c4e86-111">使用這些 Guid 來指定當您建立平板電腦內容時，封包所包含的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e86-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="c4e86-112">若要判斷屬性的範圍和解析度，請呼叫 [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) 方法。</span><span class="sxs-lookup"><span data-stu-id="c4e86-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="c4e86-113">下表中的常數（以 "STR \_ " 開頭）是在相同表格儲存格中顯示的對應二進位常數的字串表示。</span><span class="sxs-lookup"><span data-stu-id="c4e86-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c4e86-114">常數</span><span class="sxs-lookup"><span data-stu-id="c4e86-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c4e86-115">描述</span><span class="sxs-lookup"><span data-stu-id="c4e86-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="c4e86-116"><dt><strong>STR_GUID_X 或 GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-117">Tablet 座標空間中的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="c4e86-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="c4e86-118">依預設，每個封包都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e86-118">Each packet contains this property by default.</span></span> <span data-ttu-id="c4e86-119">平板電腦的原點 (0、0) 是左上角。</span><span class="sxs-lookup"><span data-stu-id="c4e86-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="c4e86-120"><dt><strong>STR_GUID_Y 或 GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-121">Tablet 座標空間中的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="c4e86-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="c4e86-122">依預設，每個封包都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e86-122">Each packet contains this property by default.</span></span> <span data-ttu-id="c4e86-123">平板電腦的原點 (0、0) 是左上角。</span><span class="sxs-lookup"><span data-stu-id="c4e86-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="c4e86-124"><dt><strong>STR_GUID_Y 或 GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-125">Tablet 座標空間中的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="c4e86-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="c4e86-126">依預設，每個封包都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e86-126">Each packet contains this property by default.</span></span> <span data-ttu-id="c4e86-127">平板電腦的原點 (0、0) 是左上角。</span><span class="sxs-lookup"><span data-stu-id="c4e86-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="c4e86-128"><dt><strong>STR_GUID_Z 或 GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-129">Tablet 介面中畫筆提示的 z 座標或距離。</span><span class="sxs-lookup"><span data-stu-id="c4e86-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="c4e86-130"><a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a>列舉型別會決定這個屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="c4e86-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="c4e86-131"><dt><strong>STR_GUID_PAKETSTATUS 或 GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-132">包含下列一或多個旗標值：</span><span class="sxs-lookup"><span data-stu-id="c4e86-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="c4e86-133">游標觸及繪圖介面 (Value = 1) 。</span><span class="sxs-lookup"><span data-stu-id="c4e86-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="c4e86-134">資料指標反轉。</span><span class="sxs-lookup"><span data-stu-id="c4e86-134">The cursor is inverted.</span></span> <span data-ttu-id="c4e86-135">例如，畫筆的橡皮擦末端指向介面 (值 = 2) 。</span><span class="sxs-lookup"><span data-stu-id="c4e86-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="c4e86-136">未使用 (值 = 4) 。</span><span class="sxs-lookup"><span data-stu-id="c4e86-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="c4e86-137">已按下 [圓筒] 按鈕 (值 = 8) 。</span><span class="sxs-lookup"><span data-stu-id="c4e86-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="c4e86-138"><dt><strong>STR_GUID_TIMERTICK 或 GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-139">產生封包的時間。</span><span class="sxs-lookup"><span data-stu-id="c4e86-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="c4e86-140"><dt><strong>STR_GUID_TIMERTICK 或 GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-141">產生封包的時間。</span><span class="sxs-lookup"><span data-stu-id="c4e86-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="c4e86-142"><dt><strong>STR_GUID_SERIALNUMBER 或 GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-143">用來識別封包的封包屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e86-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="c4e86-144">這是您用來從封包佇列取出封包的相同值。</span><span class="sxs-lookup"><span data-stu-id="c4e86-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="c4e86-145"><dt><strong>STR_GUID_NORMALPRESSURE 或 GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-146">畫筆提示與 tablet 介面垂直的壓力。</span><span class="sxs-lookup"><span data-stu-id="c4e86-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="c4e86-147">畫筆秘訣的壓力愈大，繪製的筆墨越多。</span><span class="sxs-lookup"><span data-stu-id="c4e86-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="c4e86-148"><dt><strong>STR_GUID_TANGENTPRESSURE 或 GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-149">畫筆提示沿著 tablet 介面平面的壓力。</span><span class="sxs-lookup"><span data-stu-id="c4e86-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="c4e86-150"><dt><strong>STR_GUID_BUTTONPRESSURE 或 GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-151">壓力敏感性按鈕的壓力。</span><span class="sxs-lookup"><span data-stu-id="c4e86-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="c4e86-152"><dt><strong>STR_GUID_XTILTORIENTATION 或 GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-153">Y、z 平面和畫筆和 y 軸平面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="c4e86-154">適用于畫筆游標。</span><span class="sxs-lookup"><span data-stu-id="c4e86-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="c4e86-155">當畫筆垂直至繪圖介面時，此值為0，而當畫筆位於垂直右方時為正數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="c4e86-156"><dt><strong>STR_GUID_YTILTORIENTATION 或 GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-157">X、z 平面和畫筆和 X 軸平面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="c4e86-158">適用于畫筆游標。</span><span class="sxs-lookup"><span data-stu-id="c4e86-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="c4e86-159">當畫筆垂直至繪圖介面時，此值為0，當畫筆向上或離使用者時，此值為正數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="c4e86-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION 或 GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-161">透過完整的圓形範圍，以順向軸旋轉指標與 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="c4e86-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="c4e86-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION 或 GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-163">畫筆軸和平板電腦表面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="c4e86-164">當畫筆平行至介面時，此值為0，當畫筆垂直至表面時，則為90。</span><span class="sxs-lookup"><span data-stu-id="c4e86-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="c4e86-165">當畫筆反轉時，值為負數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="c4e86-166"><dt><strong>STR_GUID_TWISTORIENTATION 或 GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-167">游標的順時針旋轉，大約是它自己的座標軸。</span><span class="sxs-lookup"><span data-stu-id="c4e86-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="c4e86-168"><dt><strong>STR_GUID_PITCHROTATION 或 GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-169">此封包屬性會指出提示是否高於或低於與書寫介面垂直的水平線。</span><span class="sxs-lookup"><span data-stu-id="c4e86-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c4e86-170">這需要3D 數位板。</span><span class="sxs-lookup"><span data-stu-id="c4e86-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="c4e86-171">如果提示位於行的正上方，則值為正數，如果在該行下方，則為負數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="c4e86-172">例如，如果您將畫筆放在您的前方，然後以虛數牆書寫，則如果筆尖在從您延伸到牆上的線條上方，則會是正面的。</span><span class="sxs-lookup"><span data-stu-id="c4e86-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="c4e86-173"><dt><strong>STR_GUID_ROLLROTATION 或 GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-174">畫筆的順時針旋轉圍繞其本身的軸。</span><span class="sxs-lookup"><span data-stu-id="c4e86-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c4e86-175">這需要3D 數位板。</span><span class="sxs-lookup"><span data-stu-id="c4e86-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="c4e86-176"><dt><strong>STR_GUID_YAWROTATION 或 GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-177">畫筆水準軸的水準軸水準軸左右左右左右的角度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c4e86-178">這需要3D 數位板。</span><span class="sxs-lookup"><span data-stu-id="c4e86-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="c4e86-179">如果您將畫筆放在您的前方，然後以虛數牆書寫，則零偏擺表示畫筆會與牆垂直。</span><span class="sxs-lookup"><span data-stu-id="c4e86-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="c4e86-180">如果提示位於垂直的左邊，則此值為負數，如果提示位於垂直右側則為正數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="c4e86-181"><dt><strong>STR_GUID_YAWROTATION 或 GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-182">畫筆水準軸的水準軸水準軸左右左右左右的角度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c4e86-183">這需要3D 數位板。</span><span class="sxs-lookup"><span data-stu-id="c4e86-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="c4e86-184">如果您將畫筆放在您的前方，然後以虛數牆書寫，則零偏擺表示畫筆會與牆垂直。</span><span class="sxs-lookup"><span data-stu-id="c4e86-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="c4e86-185">如果提示位於垂直的左邊，則此值為負數，如果提示位於垂直右側則為正數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="c4e86-186"><dt><strong>STR_GUID_WIDTH 或 GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-187">觸控式數位化板上的連絡人區域寬度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="c4e86-188"><dt><strong>STR_GUID_HEIGHT 或 GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-189">觸控式數位化板上的連絡人區域高度。</span><span class="sxs-lookup"><span data-stu-id="c4e86-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="c4e86-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE 或 GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-191">觸控式數位板上有手指接觸的信賴等級。</span><span class="sxs-lookup"><span data-stu-id="c4e86-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="c4e86-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID 或 GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4e86-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c4e86-193">封包的裝置連絡人識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4e86-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="c4e86-194">備註</span><span class="sxs-lookup"><span data-stu-id="c4e86-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c4e86-195">來自平板電腦硬體的所有封包值都是32位大小的整數。</span><span class="sxs-lookup"><span data-stu-id="c4e86-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4e86-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4e86-196">Requirements</span></span>



| <span data-ttu-id="c4e86-197">需求</span><span class="sxs-lookup"><span data-stu-id="c4e86-197">Requirement</span></span> | <span data-ttu-id="c4e86-198">值</span><span class="sxs-lookup"><span data-stu-id="c4e86-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e86-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4e86-199">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e86-200">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4e86-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c4e86-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4e86-201">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e86-202">都不支援</span><span class="sxs-lookup"><span data-stu-id="c4e86-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c4e86-203">標頭</span><span class="sxs-lookup"><span data-stu-id="c4e86-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4e86-204"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c4e86-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e86-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4e86-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e86-206">**IsPacketPropertySupported 方法**</span><span class="sxs-lookup"><span data-stu-id="c4e86-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="c4e86-207">**GetPropertyMetrics 方法**</span><span class="sxs-lookup"><span data-stu-id="c4e86-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="c4e86-208">**IInkTablet 介面**</span><span class="sxs-lookup"><span data-stu-id="c4e86-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




