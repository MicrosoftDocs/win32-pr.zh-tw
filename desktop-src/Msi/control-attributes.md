---
description: 如需控制項屬性的詳細資訊，請參閱您需要在控制項中建立之特定控制項的連結，以及下列清單中特定控制項屬性的連結。
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320092"
---
# <a name="control-attributes"></a><span data-ttu-id="1652e-103">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-103">Control Attributes</span></span>

<span data-ttu-id="1652e-104">如需控制項屬性的詳細資訊，請參閱您需要在 [控制項](controls.md) 中建立之特定控制項的連結，以及下列清單中特定控制項屬性的連結。</span><span class="sxs-lookup"><span data-stu-id="1652e-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="1652e-105">下列方法可用來指定控制項的屬性：</span><span class="sxs-lookup"><span data-stu-id="1652e-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="1652e-106">您可以使用 [ControlCondition 資料表](controlcondition-table.md) ，根據屬性或條件陳述式的值來停用、啟用、隱藏或顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="1652e-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="1652e-107">您也可以使用此資料表來覆寫在 [對話方塊資料表](dialog-table.md)中指定的預設控制項。</span><span class="sxs-lookup"><span data-stu-id="1652e-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="1652e-108">將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md)中的 ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="1652e-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="1652e-109">在 [屬性] 資料行中輸入屬性的識別碼，並在此資料表的 [事件] 資料行中輸入 ControlEvent 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1652e-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="1652e-110">在 [控制資料表](control-table.md)的 [屬性] 資料行中，設定控制項的控制項屬性位旗標。</span><span class="sxs-lookup"><span data-stu-id="1652e-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="1652e-111">這會在建立控制項時設定屬性。</span><span class="sxs-lookup"><span data-stu-id="1652e-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="1652e-112">某些屬性無法針對每個控制項設定，或由上述所有方法指定。</span><span class="sxs-lookup"><span data-stu-id="1652e-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="1652e-113">如需詳細資料，請參閱特定的控制項和屬性主題。</span><span class="sxs-lookup"><span data-stu-id="1652e-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="1652e-114">某些控制項屬性的初始值可以使用 [control 資料表](control-table.md)中的位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="1652e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-115">Attribute</span></span>                                          | <span data-ttu-id="1652e-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-116">Decimal</span></span> | <span data-ttu-id="1652e-117">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-117">Hexadecimal</span></span> | <span data-ttu-id="1652e-118">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="1652e-119">BiDi</span><span class="sxs-lookup"><span data-stu-id="1652e-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="1652e-120">224</span><span class="sxs-lookup"><span data-stu-id="1652e-120">224</span></span>     | <span data-ttu-id="1652e-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="1652e-121">0x000000E0</span></span>  | <span data-ttu-id="1652e-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="1652e-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="1652e-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="1652e-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="1652e-124">2</span><span class="sxs-lookup"><span data-stu-id="1652e-124">2</span></span>       | <span data-ttu-id="1652e-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1652e-125">0x00000002</span></span>  | <span data-ttu-id="1652e-126">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="1652e-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="1652e-127">間接</span><span class="sxs-lookup"><span data-stu-id="1652e-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="1652e-128">8</span><span class="sxs-lookup"><span data-stu-id="1652e-128">8</span></span>       | <span data-ttu-id="1652e-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1652e-129">0x00000008</span></span>  | <span data-ttu-id="1652e-130">**msidbControlAttributesIndirect**</span><span class="sxs-lookup"><span data-stu-id="1652e-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="1652e-131">整數控制項</span><span class="sxs-lookup"><span data-stu-id="1652e-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="1652e-132">16</span><span class="sxs-lookup"><span data-stu-id="1652e-132">16</span></span>      | <span data-ttu-id="1652e-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1652e-133">0x00000010</span></span>  | <span data-ttu-id="1652e-134">**msidbControlAttributesInteger**</span><span class="sxs-lookup"><span data-stu-id="1652e-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="1652e-135">LeftScroll</span><span class="sxs-lookup"><span data-stu-id="1652e-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="1652e-136">128</span><span class="sxs-lookup"><span data-stu-id="1652e-136">128</span></span>     | <span data-ttu-id="1652e-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1652e-137">0x00000080</span></span>  | <span data-ttu-id="1652e-138">**msidbControlAttributesLeftScroll**</span><span class="sxs-lookup"><span data-stu-id="1652e-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="1652e-139">RightAligned</span><span class="sxs-lookup"><span data-stu-id="1652e-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="1652e-140">64</span><span class="sxs-lookup"><span data-stu-id="1652e-140">64</span></span>      | <span data-ttu-id="1652e-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="1652e-141">0x00000040</span></span>  | <span data-ttu-id="1652e-142">**msidbControlAttributesRightAligned**</span><span class="sxs-lookup"><span data-stu-id="1652e-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="1652e-143">RTLRO</span><span class="sxs-lookup"><span data-stu-id="1652e-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="1652e-144">32</span><span class="sxs-lookup"><span data-stu-id="1652e-144">32</span></span>      | <span data-ttu-id="1652e-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="1652e-145">0x00000020</span></span>  | <span data-ttu-id="1652e-146">**msidbControlAttributesRTLRO**</span><span class="sxs-lookup"><span data-stu-id="1652e-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="1652e-147">沉沒</span><span class="sxs-lookup"><span data-stu-id="1652e-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="1652e-148">4</span><span class="sxs-lookup"><span data-stu-id="1652e-148">4</span></span>       | <span data-ttu-id="1652e-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1652e-149">0x00000004</span></span>  | <span data-ttu-id="1652e-150">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="1652e-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="1652e-151">Visible</span><span class="sxs-lookup"><span data-stu-id="1652e-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="1652e-152">1</span><span class="sxs-lookup"><span data-stu-id="1652e-152">1</span></span>       | <span data-ttu-id="1652e-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1652e-153">0x00000001</span></span>  | <span data-ttu-id="1652e-154">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="1652e-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="1652e-155">這些文字控制項的屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="1652e-156">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-156">Attribute</span></span>                                            | <span data-ttu-id="1652e-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-157">Decimal</span></span> | <span data-ttu-id="1652e-158">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-158">Hexadecimal</span></span> | <span data-ttu-id="1652e-159">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="1652e-160">FormatSize</span><span class="sxs-lookup"><span data-stu-id="1652e-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="1652e-161">524288</span><span class="sxs-lookup"><span data-stu-id="1652e-161">524288</span></span>  | <span data-ttu-id="1652e-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1652e-162">0x00080000</span></span>  | <span data-ttu-id="1652e-163">**msidbControlAttributesFormatSize**</span><span class="sxs-lookup"><span data-stu-id="1652e-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="1652e-164">NoPrefix</span><span class="sxs-lookup"><span data-stu-id="1652e-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="1652e-165">131072</span><span class="sxs-lookup"><span data-stu-id="1652e-165">131072</span></span>  | <span data-ttu-id="1652e-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1652e-166">0x00020000</span></span>  | <span data-ttu-id="1652e-167">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="1652e-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="1652e-168">NoWrap</span><span class="sxs-lookup"><span data-stu-id="1652e-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="1652e-169">262144</span><span class="sxs-lookup"><span data-stu-id="1652e-169">262144</span></span>  | <span data-ttu-id="1652e-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1652e-170">0x00040000</span></span>  | <span data-ttu-id="1652e-171">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="1652e-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="1652e-172">密碼</span><span class="sxs-lookup"><span data-stu-id="1652e-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="1652e-173">2097152</span><span class="sxs-lookup"><span data-stu-id="1652e-173">2097152</span></span> | <span data-ttu-id="1652e-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1652e-174">0x00200000</span></span>  | <span data-ttu-id="1652e-175">**msidbControlAttributesPasswordInput**</span><span class="sxs-lookup"><span data-stu-id="1652e-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="1652e-176">透明</span><span class="sxs-lookup"><span data-stu-id="1652e-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="1652e-177">65536</span><span class="sxs-lookup"><span data-stu-id="1652e-177">65536</span></span>   | <span data-ttu-id="1652e-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1652e-178">0x00010000</span></span>  | <span data-ttu-id="1652e-179">**msidbControlAttributesTransparent**</span><span class="sxs-lookup"><span data-stu-id="1652e-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="1652e-180">UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="1652e-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="1652e-181">1048576</span><span class="sxs-lookup"><span data-stu-id="1652e-181">1048576</span></span> | <span data-ttu-id="1652e-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1652e-182">0x00100000</span></span>  | <span data-ttu-id="1652e-183">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="1652e-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="1652e-184">ProgressBar 控制項的這個屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="1652e-185">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-185">Attribute</span></span>                                      | <span data-ttu-id="1652e-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-186">Decimal</span></span> | <span data-ttu-id="1652e-187">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-187">Hexadecimal</span></span> | <span data-ttu-id="1652e-188">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="1652e-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="1652e-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="1652e-190">65536</span><span class="sxs-lookup"><span data-stu-id="1652e-190">65536</span></span>   | <span data-ttu-id="1652e-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1652e-191">0x00010000</span></span>  | <span data-ttu-id="1652e-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="1652e-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="1652e-193">這些磁片區和目錄 SelectCombo 控制項的屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="1652e-194">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-194">Attribute</span></span>                                                | <span data-ttu-id="1652e-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-195">Decimal</span></span> | <span data-ttu-id="1652e-196">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-196">Hexadecimal</span></span> | <span data-ttu-id="1652e-197">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="1652e-198">CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="1652e-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="1652e-199">524288</span><span class="sxs-lookup"><span data-stu-id="1652e-199">524288</span></span>  | <span data-ttu-id="1652e-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1652e-200">0x00080000</span></span>  | <span data-ttu-id="1652e-201">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="1652e-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="1652e-202">FixedVolume</span><span class="sxs-lookup"><span data-stu-id="1652e-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="1652e-203">131072</span><span class="sxs-lookup"><span data-stu-id="1652e-203">131072</span></span>  | <span data-ttu-id="1652e-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1652e-204">0x00020000</span></span>  | <span data-ttu-id="1652e-205">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="1652e-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="1652e-206">FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="1652e-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="1652e-207">2097152</span><span class="sxs-lookup"><span data-stu-id="1652e-207">2097152</span></span> | <span data-ttu-id="1652e-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1652e-208">0x00200000</span></span>  | <span data-ttu-id="1652e-209">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="1652e-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="1652e-210">RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="1652e-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="1652e-211">1048576</span><span class="sxs-lookup"><span data-stu-id="1652e-211">1048576</span></span> | <span data-ttu-id="1652e-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1652e-212">0x00100000</span></span>  | <span data-ttu-id="1652e-213">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="1652e-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="1652e-214">RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="1652e-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="1652e-215">262144</span><span class="sxs-lookup"><span data-stu-id="1652e-215">262144</span></span>  | <span data-ttu-id="1652e-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1652e-216">0x00040000</span></span>  | <span data-ttu-id="1652e-217">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="1652e-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="1652e-218">RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="1652e-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="1652e-219">65536</span><span class="sxs-lookup"><span data-stu-id="1652e-219">65536</span></span>   | <span data-ttu-id="1652e-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1652e-220">0x00010000</span></span>  | <span data-ttu-id="1652e-221">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="1652e-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="1652e-222">ListBox 和 ComboBox 控制項的這些屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="1652e-223">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-223">Attribute</span></span>                                            | <span data-ttu-id="1652e-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-224">Decimal</span></span> | <span data-ttu-id="1652e-225">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-225">Hexadecimal</span></span> | <span data-ttu-id="1652e-226">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="1652e-227">ComboList 控制項</span><span class="sxs-lookup"><span data-stu-id="1652e-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="1652e-228">131072</span><span class="sxs-lookup"><span data-stu-id="1652e-228">131072</span></span>  | <span data-ttu-id="1652e-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1652e-229">0x00020000</span></span>  | <span data-ttu-id="1652e-230">**msidbControlAttributesComboList**</span><span class="sxs-lookup"><span data-stu-id="1652e-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="1652e-231">排序的控制項</span><span class="sxs-lookup"><span data-stu-id="1652e-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="1652e-232">65536</span><span class="sxs-lookup"><span data-stu-id="1652e-232">65536</span></span>   | <span data-ttu-id="1652e-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1652e-233">0x00010000</span></span>  | <span data-ttu-id="1652e-234">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="1652e-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="1652e-235">編輯控制項的這個屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="1652e-236">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-236">Attribute</span></span>                                    | <span data-ttu-id="1652e-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-237">Decimal</span></span> | <span data-ttu-id="1652e-238">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-238">Hexadecimal</span></span> | <span data-ttu-id="1652e-239">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="1652e-240">適用</span><span class="sxs-lookup"><span data-stu-id="1652e-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="1652e-241">65536</span><span class="sxs-lookup"><span data-stu-id="1652e-241">65536</span></span>   | <span data-ttu-id="1652e-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="1652e-242">0x00010000</span></span>  | <span data-ttu-id="1652e-243">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="1652e-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="1652e-244">這些 PictureButton 控制項的屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="1652e-245">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-245">Attribute</span></span>                                          | <span data-ttu-id="1652e-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-246">Decimal</span></span> | <span data-ttu-id="1652e-247">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-247">Hexadecimal</span></span> | <span data-ttu-id="1652e-248">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="1652e-249">點陣圖</span><span class="sxs-lookup"><span data-stu-id="1652e-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="1652e-250">262144</span><span class="sxs-lookup"><span data-stu-id="1652e-250">262144</span></span>  | <span data-ttu-id="1652e-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1652e-251">0x00040000</span></span>  | <span data-ttu-id="1652e-252">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="1652e-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="1652e-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="1652e-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="1652e-254">1048576</span><span class="sxs-lookup"><span data-stu-id="1652e-254">1048576</span></span> | <span data-ttu-id="1652e-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1652e-255">0x00100000</span></span>  | <span data-ttu-id="1652e-256">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="1652e-256">**msidbControlAttributesFixedSize**</span></span>  |
| [<span data-ttu-id="1652e-257">圖示</span><span class="sxs-lookup"><span data-stu-id="1652e-257">Icon</span></span>](icon-control-attribute.md)                 | <span data-ttu-id="1652e-258">524288</span><span class="sxs-lookup"><span data-stu-id="1652e-258">524288</span></span>  | <span data-ttu-id="1652e-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="1652e-259">0x00080000</span></span>  | <span data-ttu-id="1652e-260">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="1652e-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="1652e-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="1652e-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="1652e-262">2097152</span><span class="sxs-lookup"><span data-stu-id="1652e-262">2097152</span></span> | <span data-ttu-id="1652e-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="1652e-263">0x00200000</span></span>  | <span data-ttu-id="1652e-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="1652e-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="1652e-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="1652e-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="1652e-266">4194304</span><span class="sxs-lookup"><span data-stu-id="1652e-266">4194304</span></span> | <span data-ttu-id="1652e-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="1652e-267">0x00400000</span></span>  | <span data-ttu-id="1652e-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="1652e-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="1652e-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="1652e-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="1652e-270">6291456</span><span class="sxs-lookup"><span data-stu-id="1652e-270">6291456</span></span> | <span data-ttu-id="1652e-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="1652e-271">0x00600000</span></span>  | <span data-ttu-id="1652e-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="1652e-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="1652e-273">PushLike 控制項</span><span class="sxs-lookup"><span data-stu-id="1652e-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="1652e-274">131072</span><span class="sxs-lookup"><span data-stu-id="1652e-274">131072</span></span>  | <span data-ttu-id="1652e-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1652e-275">0x00020000</span></span>  | <span data-ttu-id="1652e-276">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="1652e-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="1652e-277">選項按鈕控制項的這個屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="1652e-278">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-278">Attribute</span></span>                                    | <span data-ttu-id="1652e-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-279">Decimal</span></span>  | <span data-ttu-id="1652e-280">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-280">Hexadecimal</span></span> | <span data-ttu-id="1652e-281">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="1652e-282">HasBorder</span><span class="sxs-lookup"><span data-stu-id="1652e-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="1652e-283">16777216</span><span class="sxs-lookup"><span data-stu-id="1652e-283">16777216</span></span> | <span data-ttu-id="1652e-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="1652e-284">0x01000000</span></span>  | <span data-ttu-id="1652e-285">**msidbControlAttributesHasBorder**</span><span class="sxs-lookup"><span data-stu-id="1652e-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="1652e-286">此按鈕控制項的這個屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="1652e-287">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-287">Attribute</span></span>                                        | <span data-ttu-id="1652e-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-288">Decimal</span></span> | <span data-ttu-id="1652e-289">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-289">Hexadecimal</span></span> | <span data-ttu-id="1652e-290">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="1652e-291">ElevationShield</span><span class="sxs-lookup"><span data-stu-id="1652e-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="1652e-292">8388608</span><span class="sxs-lookup"><span data-stu-id="1652e-292">8388608</span></span> | <span data-ttu-id="1652e-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="1652e-293">0x00800000</span></span>  | <span data-ttu-id="1652e-294">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="1652e-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="1652e-295">VolumeCostList 控制項的這個屬性是以位來設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="1652e-296">屬性</span><span class="sxs-lookup"><span data-stu-id="1652e-296">Attribute</span></span>                                                                | <span data-ttu-id="1652e-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="1652e-297">Decimal</span></span> | <span data-ttu-id="1652e-298">十六進位</span><span class="sxs-lookup"><span data-stu-id="1652e-298">Hexadecimal</span></span> | <span data-ttu-id="1652e-299">常數</span><span class="sxs-lookup"><span data-stu-id="1652e-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="1652e-300">ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="1652e-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="1652e-301">4194304</span><span class="sxs-lookup"><span data-stu-id="1652e-301">4194304</span></span> | <span data-ttu-id="1652e-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="1652e-302">0x00400000</span></span>  | <span data-ttu-id="1652e-303">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="1652e-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="1652e-304">下列控制項屬性不是以位設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="1652e-305">這些屬性會編寫到使用者介面資料表中，或使用 [控制項事件](control-events.md)進行設定。</span><span class="sxs-lookup"><span data-stu-id="1652e-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="1652e-306">BillboardName</span><span class="sxs-lookup"><span data-stu-id="1652e-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="1652e-307">IndirectPropertyName</span><span class="sxs-lookup"><span data-stu-id="1652e-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="1652e-308">位置</span><span class="sxs-lookup"><span data-stu-id="1652e-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="1652e-309">進度控制項</span><span class="sxs-lookup"><span data-stu-id="1652e-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="1652e-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="1652e-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="1652e-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="1652e-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="1652e-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="1652e-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="1652e-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="1652e-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="1652e-314">請參閱 [加入控制項和文字](adding-controls-and-text.md)。</span><span class="sxs-lookup"><span data-stu-id="1652e-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 



