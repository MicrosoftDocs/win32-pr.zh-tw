---
description: 除非在其描述中另有說明，否則所有 IWiaItem、IWiaItem2 和 IWiaDrvItem 介面介面都必須支援下列裝置屬性常數。
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: '常見的 WIA 專案屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967142"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="2ca53-103">常見的 WIA 專案屬性常數</span><span class="sxs-lookup"><span data-stu-id="2ca53-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="2ca53-104">除非在其描述中另有說明，否則所有 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)、 [**IWiaItem2**](-wia-iwiaitem2.md) 和 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 介面都必須支援下列裝置屬性常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="2ca53-105">前置詞 "WIA \_ IPA \_ " 表示所有裝置的專案屬性，而且是 C/c + + 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="2ca53-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="2ca53-106">在撰寫腳本時，這些常數會使用前置詞「圖片」，且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="2ca53-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="2ca53-107">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="2ca53-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2ca53-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="2ca53-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2ca53-109">Description</span><span class="sxs-lookup"><span data-stu-id="2ca53-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="2ca53-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2ca53-111">此旗標會控制專案的存取權，以及是否刪除專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="2ca53-112">所有 WIA 2.0 專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="2ca53-113">類型： <strong>VT_I4</strong>;[讀取/寫入] 或 [唯讀]，視專案的存取權限變更的能力而定;有效的值： WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="2ca53-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="2ca53-114">下表有五個對此屬性有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="2ca53-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-115">存取權限</span><span class="sxs-lookup"><span data-stu-id="2ca53-115">Access Right</span></span></th>
<th><span data-ttu-id="2ca53-116">Description</span><span class="sxs-lookup"><span data-stu-id="2ca53-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="2ca53-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="2ca53-118">專案具有唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="2ca53-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="2ca53-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="2ca53-120">專案具有僅限寫入的存取權。</span><span class="sxs-lookup"><span data-stu-id="2ca53-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="2ca53-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="2ca53-122">專案具有僅限刪除的存取權。</span><span class="sxs-lookup"><span data-stu-id="2ca53-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="2ca53-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="2ca53-124">WIA_ITEM_READ |WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="2ca53-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="2ca53-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="2ca53-126">WIA_ITEM_READ |WIA_ITEM_WRITE |WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="2ca53-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="2ca53-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-128">這個屬性是保留供日後使用，且目前不會執行。</span><span class="sxs-lookup"><span data-stu-id="2ca53-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="2ca53-129">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="2ca53-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-131">包含影像每個通道的位數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="2ca53-132">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-133">所有 WIA 2.0 取得啟用或預存映射專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="2ca53-134">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="2ca53-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-136">包含資料傳輸期間使用的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2ca53-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="2ca53-137">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-138">應用程式可以讀取此屬性，以判斷用於資料傳輸的驅動程式指定緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2ca53-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="2ca53-139">WIA 服務也會在資料傳輸期間，讀取此屬性以配置迷你驅動程式的記憶體</span><span class="sxs-lookup"><span data-stu-id="2ca53-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="2ca53-140">所有已啟用轉換的 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-141">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2ca53-142"><strong>WIA_IPA_BUFFER_SIZE</strong>屬性包含的是應用程式在任何指定時間可以要求的最小資料量。</span><span class="sxs-lookup"><span data-stu-id="2ca53-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="2ca53-143">緩衝區大小愈大，裝置的要求就會愈大。</span><span class="sxs-lookup"><span data-stu-id="2ca53-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="2ca53-144">這可能使裝置看起來很慢且沒有回應，可能會降低整體系統效能，並且可能耗用過多的資源。</span><span class="sxs-lookup"><span data-stu-id="2ca53-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="2ca53-145">緩衝區大小太小可能會要求許多較小的要求，使資料傳輸的效能變慢。</span><span class="sxs-lookup"><span data-stu-id="2ca53-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="2ca53-146">請考慮您裝置的一般資料要求大小，並根據這些要求的大小來平衡要求數目，以選擇合理的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2ca53-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="2ca53-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-148">包含影像的一個掃描行中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2ca53-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="2ca53-149">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-150">所有 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-151">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="2ca53-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-153">包含影像每圖元的通道數目。</span><span class="sxs-lookup"><span data-stu-id="2ca53-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="2ca53-154">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-155">所有 WIA 2.0 取得啟用或預存映射專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="2ca53-156">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="2ca53-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-158">這個屬性是保留供日後使用，且目前不會執行。</span><span class="sxs-lookup"><span data-stu-id="2ca53-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="2ca53-159">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="2ca53-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-161">包含目前使用的壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="2ca53-161">Contains the current compression type used.</span></span> <span data-ttu-id="2ca53-162">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-163">應用程式會讀取這個屬性，以判斷影像壓縮類型，或設定這個屬性來設定壓縮設定。</span><span class="sxs-lookup"><span data-stu-id="2ca53-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="2ca53-164">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2ca53-165">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="2ca53-166"><strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="2ca53-167"> (只能透過 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 介面使用。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-168">[壓縮類型]</span><span class="sxs-lookup"><span data-stu-id="2ca53-168">Compression Type</span></span></th>
<th><span data-ttu-id="2ca53-169">Description</span><span class="sxs-lookup"><span data-stu-id="2ca53-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="2ca53-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="2ca53-171">無壓縮。</span><span class="sxs-lookup"><span data-stu-id="2ca53-171">No compression.</span></span> <span data-ttu-id="2ca53-172">如需詳細資訊，請參閱 <strong>備註</strong> 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="2ca53-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="2ca53-174">自動壓縮模式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-174">Automatic compression mode.</span></span> <span data-ttu-id="2ca53-175">如需詳細資訊，請參閱 <strong>備註</strong> 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="2ca53-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="2ca53-177">RLE4 壓縮</span><span class="sxs-lookup"><span data-stu-id="2ca53-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="2ca53-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="2ca53-179">RLE8 壓縮</span><span class="sxs-lookup"><span data-stu-id="2ca53-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="2ca53-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="2ca53-181">群組3壓縮</span><span class="sxs-lookup"><span data-stu-id="2ca53-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="2ca53-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="2ca53-183">群組4壓縮</span><span class="sxs-lookup"><span data-stu-id="2ca53-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="2ca53-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="2ca53-185">JPEG 壓縮。</span><span class="sxs-lookup"><span data-stu-id="2ca53-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-187">JBIG 壓縮。</span><span class="sxs-lookup"><span data-stu-id="2ca53-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-189">JPEG 2000 壓縮。</span><span class="sxs-lookup"><span data-stu-id="2ca53-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-191">PNG 壓縮。</span><span class="sxs-lookup"><span data-stu-id="2ca53-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="2ca53-192">當 WIA_COMPRESSION_NONE 這個屬性時，WIA_IPA_FORMAT 是 WiaImgFmt_PDFA 或 WiaImgFmt_XPS;然後 WIA_COMPRESSION_NONE 表示壓縮模式是未定義的，而且掃描器必須決定模式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="2ca53-193">WIA_COMPRESSION_AUTO 是針對 WIA_IPA_COMPRESSION 屬性定義的新屬性值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="2ca53-194">此值適用于所有可程式化的影像資料來源專案，包括平板和送紙器。</span><span class="sxs-lookup"><span data-stu-id="2ca53-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="2ca53-195">當 WIA 迷你驅動程式支援這個值時，WIA 應用程式用戶端可以設定 WIA_IPA_COMPRESSION，以便在裝置上啟用自動壓縮模式偵測。</span><span class="sxs-lookup"><span data-stu-id="2ca53-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="2ca53-196">WIA_COMPRESSION_AUTO 可以搭配使用，而且不會支援或啟用完整的自動色彩 (WIA_DATA_AUTO 和 WIA_DEPTH_AUTO) 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="2ca53-197">WIA_COMPRESSION_AUTO 最適合用於支援多種資料類型和位深度的傳輸檔案格式，例如 WiaImgFmt_RAW。</span><span class="sxs-lookup"><span data-stu-id="2ca53-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="2ca53-198">如需傳輸檔案格式的詳細資訊，請參閱此表格中的 WIA_IPA_FORMAT。</span><span class="sxs-lookup"><span data-stu-id="2ca53-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="2ca53-199">它的 opitonal 是要讓 WIA 迷你驅動程式支援 WIA_COMPRESSION_AUTO。</span><span class="sxs-lookup"><span data-stu-id="2ca53-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="2ca53-200">當支援時，WIA 迷你驅動程式絕對不能將它設為 WIA_IPA_COMPRESSION 的預設值;只有 WIA 應用程式可以設定此值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="2ca53-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-202">包含裝置目前的資料類型設定。</span><span class="sxs-lookup"><span data-stu-id="2ca53-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="2ca53-203">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-204">應用程式會讀取這個屬性，以判斷影像的資料類型。</span><span class="sxs-lookup"><span data-stu-id="2ca53-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="2ca53-205">應用程式會寫入這個屬性，以設定即將傳送之影像的目前資料類型。</span><span class="sxs-lookup"><span data-stu-id="2ca53-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="2ca53-206">所有 WIA 2.0 專案都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="2ca53-207">它必須針對所有啟用 WIA 2.0 的已啟用專案進行讀取/寫入，並唯讀取 WIA 2.0 儲存體專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="2ca53-208">類型： <strong>VT_I4</strong>;Windows Vista 前版作業系統的存取權：此屬性是唯讀的，適用于相機和讀取/寫入掃描器;Windows Vista 和更新版本的存取：此屬性是唯讀的，適用于 WIA_CATEGORY_FOLDER 和 WIA_CATEGORY_FINISHED_FILE 專案，以及所有其他 WIA 2.0 專案類別目錄的讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2ca53-209">下表具有六個在 <strong>WIA_IPA_FORMAT</strong> 未設定為 WiaImgFmt_RAW 時有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-210">資料類型</span><span class="sxs-lookup"><span data-stu-id="2ca53-210">Data Type</span></span></th>
<th><span data-ttu-id="2ca53-211">描述</span><span class="sxs-lookup"><span data-stu-id="2ca53-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="2ca53-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="2ca53-213">適用于所有可程式化的影像資料來源專案，包括平板和送紙器。</span><span class="sxs-lookup"><span data-stu-id="2ca53-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="2ca53-214">當 WIA 迷你驅動程式支援這個值時，WIA 應用程式用戶端可以設定 WIA_IPA_DATATYPE，以便在裝置上啟用自動色彩偵測。</span><span class="sxs-lookup"><span data-stu-id="2ca53-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="2ca53-215">設定 WIA_DATA_AUTO 時，WIA 迷你驅動程式必須將相同專案上的 WIA_IPA_DEPTH 更新為 WIA_DEPTH_AUTO (如果裝置支援自動色彩) ，則必須是支援的值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="2ca53-216">這是選擇性的值，但 WIA_DEPTH_AUTO 支援 WIA_IPA_DEPTH 時則需要。</span><span class="sxs-lookup"><span data-stu-id="2ca53-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="2ca53-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="2ca53-218">掃描資料是紅色、綠色、藍色 (RGB) 色彩。</span><span class="sxs-lookup"><span data-stu-id="2ca53-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="2ca53-219">使用下列 WIA 屬性來描述完整色彩格式： <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="2ca53-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="2ca53-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="2ca53-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="2ca53-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="2ca53-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="2ca53-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="2ca53-226">與 WIA_DATA_COLOR 相同，不同之處在于資料是使用目前選取的遞色模式進行遞色。</span><span class="sxs-lookup"><span data-stu-id="2ca53-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="2ca53-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="2ca53-228">與 WIA_DATA_COLOR 相同，不同之處在于掃描資料時使用臨界值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="2ca53-229"><a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a>值的色彩值會轉換成完整亮度;此值下的色彩會轉換為黑色。</span><span class="sxs-lookup"><span data-stu-id="2ca53-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="2ca53-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="2ca53-231">掃描資料是使用目前選取的遞色模式進行遞色。</span><span class="sxs-lookup"><span data-stu-id="2ca53-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="2ca53-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="2ca53-233">掃描資料代表濃度。</span><span class="sxs-lookup"><span data-stu-id="2ca53-233">Scan data represents intensity.</span></span> <span data-ttu-id="2ca53-234">此調色板是固定且等距的灰色小數位數，並以 <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> 屬性指定深度。</span><span class="sxs-lookup"><span data-stu-id="2ca53-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="2ca53-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="2ca53-236">閾值是黑色和白色資料的每個圖元一位。</span><span class="sxs-lookup"><span data-stu-id="2ca53-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="2ca53-237"><a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a>的目前值資料會轉換成白色;此值下的資料會轉換為黑色。</span><span class="sxs-lookup"><span data-stu-id="2ca53-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2ca53-238"><strong>WIA_IPA_DATATYPE</strong>屬性也用來描述當應用程式設定 WiaImgFmt_RAW 時要使用的原始資料傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="2ca53-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="2ca53-239">驅動程式應該將 <strong>WIA_IPA_DATATYPE</strong> 屬性設定為允許的值清單，讓應用程式可從中挑選一個值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="2ca53-240">如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="2ca53-241">檢查 <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> 屬性以判斷位深度。</span><span class="sxs-lookup"><span data-stu-id="2ca53-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="2ca53-242">這個屬性通常會包含相機的單一值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="2ca53-243">下表列出<strong>WIA_IPA_FORMAT</strong>設定為 WiaImgFmt_RAW 時，對<strong>WIA_IPA_DATATYPE</strong>有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-244">資料類型</span><span class="sxs-lookup"><span data-stu-id="2ca53-244">Data Type</span></span></th>
<th><span data-ttu-id="2ca53-245">描述</span><span class="sxs-lookup"><span data-stu-id="2ca53-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="2ca53-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="2ca53-247">掃描資料代表濃度。</span><span class="sxs-lookup"><span data-stu-id="2ca53-247">Scan data represents intensity.</span></span> <span data-ttu-id="2ca53-248">此調色板是固定且等距的灰色，以及 <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> 屬性指定的深度。</span><span class="sxs-lookup"><span data-stu-id="2ca53-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="2ca53-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="2ca53-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="2ca53-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="2ca53-251">掃描資料位於 BGR (藍-綠-red) colorspace。</span><span class="sxs-lookup"><span data-stu-id="2ca53-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="2ca53-252">使用 followingWIAproperties 來描述完整的色彩格式： <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="2ca53-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="2ca53-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="2ca53-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="2ca53-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="2ca53-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。</span><span class="sxs-lookup"><span data-stu-id="2ca53-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="2ca53-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="2ca53-259">掃描資料為青色-洋紅-黃色 (CMY) colorspace。</span><span class="sxs-lookup"><span data-stu-id="2ca53-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="2ca53-260">使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="2ca53-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。</span><span class="sxs-lookup"><span data-stu-id="2ca53-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="2ca53-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="2ca53-263">掃描資料是以青色-洋紅-黃色-黑色 (CMYK) colorspace。</span><span class="sxs-lookup"><span data-stu-id="2ca53-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="2ca53-264">使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="2ca53-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設定為4。</span><span class="sxs-lookup"><span data-stu-id="2ca53-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="2ca53-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="2ca53-267">掃描資料是以紅色-綠色-藍色 (RGB) colorspace。</span><span class="sxs-lookup"><span data-stu-id="2ca53-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="2ca53-268">使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="2ca53-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。</span><span class="sxs-lookup"><span data-stu-id="2ca53-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="2ca53-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="2ca53-271">掃描資料的亮度-藍色差異-紅色差異 (YUV) colorspace。</span><span class="sxs-lookup"><span data-stu-id="2ca53-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="2ca53-272">使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="2ca53-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。</span><span class="sxs-lookup"><span data-stu-id="2ca53-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="2ca53-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="2ca53-275">掃描資料處於 [亮度-藍色差異-紅色差異-黑色] (YUVK) colorspace]。</span><span class="sxs-lookup"><span data-stu-id="2ca53-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="2ca53-276">使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="2ca53-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設定為4。</span><span class="sxs-lookup"><span data-stu-id="2ca53-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="2ca53-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-279">WIA_IPA_DEPTH 包含影像的位深度設定。</span><span class="sxs-lookup"><span data-stu-id="2ca53-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="2ca53-280">迷你驅動程式會建立並維護此屬性。應用程式會讀取這個屬性，以判斷影像的位深度設定。</span><span class="sxs-lookup"><span data-stu-id="2ca53-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="2ca53-281">此應用程式也可以將此值設定為所需的位深度。</span><span class="sxs-lookup"><span data-stu-id="2ca53-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="2ca53-282">如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="2ca53-283">所有 WIA 2.0 專案都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="2ca53-284">它必須針對所有啟用 WIA 2.0 的已啟用專案進行讀取/寫入，並唯讀取 WIA 2.0 儲存體專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="2ca53-285">類型： <strong>VT_I4</strong>;Windows Vista 前版作業系統的存取權：讀取/寫入;Windows Vista 和更新版本的存取：此屬性是唯讀的，適用于 WIA_CATEGORY_FOLDER 和 WIA_CATEGORY_FINISHED_FILE 專案，以及所有其他 WIA 2.0 專案類別目錄的讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2ca53-286">WIA_DEPTH_AUTO 定義為每圖元0位，而且是為 WIA_IPA_DEPTH 定義的新屬性值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="2ca53-287">此值適用于所有可程式化的影像資料來源專案，包括平板和送紙器。</span><span class="sxs-lookup"><span data-stu-id="2ca53-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="2ca53-288">當 WIA 迷你驅動程式支援 WIA_DEPTH_AUTO 時，WIA 應用程式用戶端可以將 WIA_IPA_DEPTH 設定為此值，以在裝置上啟用自動色彩偵測。</span><span class="sxs-lookup"><span data-stu-id="2ca53-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="2ca53-289">當 WIA_DEPTH_AUTO 設定時，如果裝置支援自動色彩) ，則 WIA 迷你驅動程式必須將相同專案上的 WIA_IPA_DATATYPE 更新為 WIA_DATA_AUTO (必須是支援的值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="2ca53-290">WIA_DEPTH_AUTO 是選擇性的值，但是當 WIA_IPA_DATATYPE 支援 WIA_DATA_AUTO 時，就會變成必要值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="2ca53-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-292">包含特定檔案格式的副檔名。</span><span class="sxs-lookup"><span data-stu-id="2ca53-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="2ca53-293">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-294">所有已啟用轉換的 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-295">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2ca53-296">驅動程式會更新這個屬性，以反映 <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> 屬性的目前值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="2ca53-297">例如，如果 WiaImgFmt_JPEG <strong>WIA_IPA_FORMAT</strong> ，則 <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> 應該是 <strong>jpg</strong>。</span><span class="sxs-lookup"><span data-stu-id="2ca53-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="2ca53-298">如果 WiaImgFmt_BMP <strong>WIA_IPA_FORMAT</strong> ，則 WIA_IPA_FILENAME_EXTENSION 應該是 BMP。</span><span class="sxs-lookup"><span data-stu-id="2ca53-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2ca53-299">副檔名不包含點。</span><span class="sxs-lookup"><span data-stu-id="2ca53-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2ca53-300">針對支援標準格式的驅動程式，建議使用此屬性，並針對執行自訂定義格式的驅動程式需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="2ca53-301">它會通知應用程式正確的副檔名，以便在私用格式化的檔案傳送期間使用。</span><span class="sxs-lookup"><span data-stu-id="2ca53-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="2ca53-302">例如，如果 a. Datum Corporation 建立了以新格式傳送檔案的 WIA 驅動程式，該公司就可以指定 adc 的延伸 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="2ca53-303">這可讓應用程式將該格式的資料傳輸至檔案，並建立檔案名（例如 <em>myfile.txt</em>），這對其他瞭解新擴充功能的人很有用。</span><span class="sxs-lookup"><span data-stu-id="2ca53-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="2ca53-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-305">包含要傳送的目前影像格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="2ca53-306">應用程式會讀取此屬性，以判斷其即將接收的影像格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="2ca53-307">應用程式會寫入這個屬性來設定格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-307">An application writes this property to set the format.</span></span> <span data-ttu-id="2ca53-308">這個屬性相依于 <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="2ca53-309">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-310">如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="2ca53-311">類型： <strong>CLSID</strong>，存取：讀取/寫入，有效值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2ca53-312">下表列出對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="2ca53-313">星號 \* 表示 Windows Vista 中不支援常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="2ca53-314"> (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) 雙星號\ *\ * 表示 windows Server 2003 或 windows Vista 中不支援該常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="2ca53-315"><strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="2ca53-316"> (只能透過 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 介面使用。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-317">格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-317">Format</span></span></th>
<th><span data-ttu-id="2ca53-318">描述</span><span class="sxs-lookup"><span data-stu-id="2ca53-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="2ca53-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="2ca53-320">.AIFF 音訊格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="2ca53-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="2ca53-322">MP3 音訊格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="2ca53-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="2ca53-324">WAV 音訊格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="2ca53-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="2ca53-326">WMA 音訊格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="2ca53-328">ASF 影片格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="2ca53-330">AVI 影片格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="2ca53-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="2ca53-332">具有標頭檔的 Windows 點陣圖</span><span class="sxs-lookup"><span data-stu-id="2ca53-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="2ca53-334">相機影像檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="2ca53-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="2ca53-336">DPOF 列印格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="2ca53-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="2ca53-338">擴充的 Windows 中繼檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="2ca53-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="2ca53-340">執行檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="2ca53-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="2ca53-342">交換檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="2ca53-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="2ca53-344">FlashPix 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="2ca53-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="2ca53-346">GIF 影像格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="2ca53-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="2ca53-348">HTML 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="2ca53-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="2ca53-350">Windows 圖示檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-352">聯合 Bi 層級影像專家群組 (JBIG) 格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="2ca53-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="2ca53-354">JPEG 壓縮格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="2ca53-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="2ca53-356">JPEG 2000 壓縮格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="2ca53-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="2ca53-358">JPEG 2000 壓縮格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="2ca53-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="2ca53-360">沒有標頭檔的 Windows 點陣圖</span><span class="sxs-lookup"><span data-stu-id="2ca53-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-362">PDF/A (ISO/CD 19005-1) 格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="2ca53-364">MPEG 影片格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="2ca53-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="2ca53-366">Eastman Kodak 檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="2ca53-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="2ca53-368">Apple 檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="2ca53-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="2ca53-370">W3C PNG 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="2ca53-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="2ca53-372">僅適用于資料傳輸的 Raw 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="2ca53-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="2ca53-374">Raw RGB 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="2ca53-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="2ca53-376">Rich Text 檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="2ca53-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="2ca53-378">指令碼檔案</span><span class="sxs-lookup"><span data-stu-id="2ca53-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="2ca53-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="2ca53-380">TIF 檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="2ca53-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="2ca53-382">文字檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="2ca53-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="2ca53-384">UNICODE 16 位編碼</span><span class="sxs-lookup"><span data-stu-id="2ca53-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="2ca53-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="2ca53-386">Windows 中繼檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="2ca53-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="2ca53-388">XML 檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-390">XPS 封裝格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2ca53-391">當這個屬性是 WiaImgFmt_PDFA 或 WiaImgFmt_XPS，而且 WIA_IPA_COMPRESSION 是 WIA_COMPRESSION_NONE 時，接著，第二個值表示壓縮模式是未定義的，而且掃描器必須決定模式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="2ca53-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-393">包含專案名稱 (的完整專案名稱，以及) 的路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="2ca53-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="2ca53-394">完整專案名稱與<a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a>服務公用程式函數的<em>bstrFullItemName</em>參數相同。</span><span class="sxs-lookup"><span data-stu-id="2ca53-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="2ca53-395">應用程式會讀取這個屬性，以判斷它目前正在使用的專案，以及該專案在專案樹狀結構中的位置。</span><span class="sxs-lookup"><span data-stu-id="2ca53-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="2ca53-396">每個專案都應該要有唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca53-396">Each item should have a unique name.</span></span> <span data-ttu-id="2ca53-397">應用程式通常會使用完整專案名稱來搜尋專案樹狀結構中的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="2ca53-398">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-399">所有 WIA 2.0 專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-400">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="2ca53-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-402">這個屬性保留供日後使用，目前不會執行。</span><span class="sxs-lookup"><span data-stu-id="2ca53-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="2ca53-403">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="2ca53-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-405">包含正確解碼映射所需的 ICM 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca53-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="2ca53-406">應用程式會讀取此屬性，以判斷處理映射時所要使用的 ICM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2ca53-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="2ca53-407">WIA 服務會根據驅動程式安裝檔案中的 ICMProfiles 專案，建立及維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="2ca53-408">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="2ca53-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-410">只有在 Windows Vista 和更新版本中才支援。</span><span class="sxs-lookup"><span data-stu-id="2ca53-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="2ca53-411">WIA 2.0 專案會分組為類別，以定義如何處理或使用 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="2ca53-412">例如，如果專案代表送紙器，則應用程式應該會預期它包含所需的檔送紙器屬性，並如同檔輸送器般運作。</span><span class="sxs-lookup"><span data-stu-id="2ca53-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="2ca53-413">如果專案代表已完成的檔案，則 WIA 2.0 應用程式應該以這種方式處理，並假設資料是靜態的，而且位於裝置上。</span><span class="sxs-lookup"><span data-stu-id="2ca53-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="2ca53-414"> (每個專案的規則都會在其個別規格檔中定義。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="2ca53-415">所有 WIA 2.0 專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-416">類型： <strong>VT_CLSID</strong>、存取：唯讀、有效的值： <a href="-wia-wia2-itemcategoryguids.md"><strong>專案分類 guid</strong></a></span><span class="sxs-lookup"><span data-stu-id="2ca53-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="2ca53-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-418">包含 WIA 專案的描述性旗標。</span><span class="sxs-lookup"><span data-stu-id="2ca53-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="2ca53-419">專案旗標與<a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a>服務公用程式函式的<em>lObjectFlags</em>參數中的旗標相同。</span><span class="sxs-lookup"><span data-stu-id="2ca53-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="2ca53-420">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-421">應用程式會讀取這個屬性，以判斷專案的描述性旗標值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="2ca53-422">類型： <strong>VT_I4</strong> 存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2ca53-423">下表包含對此屬性有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="2ca53-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="2ca53-424">星號 \* 表示 Windows Vista 或更新版本中不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="2ca53-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="2ca53-425"> (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) 雙星號\ *\ * 表示 windows Server 2003 或 windows Vista 或更新版本不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="2ca53-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="2ca53-426"><strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援旗標。</span><span class="sxs-lookup"><span data-stu-id="2ca53-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="2ca53-427"> (只能透過 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 介面使用。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-428">旗標</span><span class="sxs-lookup"><span data-stu-id="2ca53-428">Flag</span></span></th>
<th><span data-ttu-id="2ca53-429">定義</span><span class="sxs-lookup"><span data-stu-id="2ca53-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-430">WiaItemTypeAnalyze\*</span><span class="sxs-lookup"><span data-stu-id="2ca53-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="2ca53-431">此專案支援 <strong>IWiaItem：： AnalyzeItem</strong> 方法 () 的 Platform SDK 檔中所述。</span><span class="sxs-lookup"><span data-stu-id="2ca53-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="2ca53-432">此專案也支援自動產生子專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="2ca53-433">這項功能適用于區域偵測或分頁分解。</span><span class="sxs-lookup"><span data-stu-id="2ca53-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-434">WiaItemTypeAudio</span><span class="sxs-lookup"><span data-stu-id="2ca53-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="2ca53-435">此專案支援音訊。</span><span class="sxs-lookup"><span data-stu-id="2ca53-435">This item supports audio.</span></span> <span data-ttu-id="2ca53-436">此旗標只適用于也已設定 <strong>WiaItemTypeFile</strong> 旗標的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-437">WiaItemTypeBurst\*</span><span class="sxs-lookup"><span data-stu-id="2ca53-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="2ca53-438">僅適用于資料夾。</span><span class="sxs-lookup"><span data-stu-id="2ca53-438">For folders only.</span></span> <span data-ttu-id="2ca53-439">此旗標表示此資料夾中的影像是以連續時間順序拍攝。</span><span class="sxs-lookup"><span data-stu-id="2ca53-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-440">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="2ca53-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="2ca53-441">此專案已標示為要刪除、此專案已被刪除、此專案不存在，或此專案的內容無效。</span><span class="sxs-lookup"><span data-stu-id="2ca53-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-442">WiaItemTypeDocument<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-443">此專案是 <strong>WIA_IPA_FORMAT</strong> 屬性包含的其中一種檔案格式的檔檔。</span><span class="sxs-lookup"><span data-stu-id="2ca53-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="2ca53-444"> (這些格式包括 nonimage 檔案的格式，例如 .txt、.htm 和 .doc 檔案。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-445">WiaItemTypeDevice</span><span class="sxs-lookup"><span data-stu-id="2ca53-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="2ca53-446">此專案代表連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="2ca53-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-447">WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="2ca53-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="2ca53-448">此專案代表已中斷連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="2ca53-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-449">WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="2ca53-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="2ca53-450">專案支援檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="2ca53-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-451">WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="2ca53-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="2ca53-452">專案是資料夾。</span><span class="sxs-lookup"><span data-stu-id="2ca53-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-453">WiaItemTypeFree</span><span class="sxs-lookup"><span data-stu-id="2ca53-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="2ca53-454">專案未初始化或已刪除。</span><span class="sxs-lookup"><span data-stu-id="2ca53-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-455">WiaItemTypeGenerated</span><span class="sxs-lookup"><span data-stu-id="2ca53-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="2ca53-456">此專案是由應用程式或驅動程式所產生。</span><span class="sxs-lookup"><span data-stu-id="2ca53-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-457">WiaItemTypeHasAttachments\*</span><span class="sxs-lookup"><span data-stu-id="2ca53-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="2ca53-458">此專案支援附件，且目前包含附件。</span><span class="sxs-lookup"><span data-stu-id="2ca53-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-459">WiaItemTypeHPanorama\*</span><span class="sxs-lookup"><span data-stu-id="2ca53-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="2ca53-460">此專案代表水準全景影像。</span><span class="sxs-lookup"><span data-stu-id="2ca53-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="2ca53-461">此旗標只適用于也已設定 <strong>WiaItemTypeFolder</strong> 旗標的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-462">WiaItemTypeImage</span><span class="sxs-lookup"><span data-stu-id="2ca53-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="2ca53-463">專案是影像檔案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-463">The item is an image file.</span></span> <span data-ttu-id="2ca53-464">此旗標只適用于也已設定 <strong>WiaItemTypeFile</strong> 旗標的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-466">此專案是可程式化的資料來源，並遵循一組預先定義的設定規則，這些規則是以 <strong>WIA_IPA_ITEM_CATEGORY</strong>為基礎。</span><span class="sxs-lookup"><span data-stu-id="2ca53-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-467">WiaItemTypeRoot<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2ca53-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="2ca53-468">此專案是根項目，也就是裝置支援的所有功能專案的父系。</span><span class="sxs-lookup"><span data-stu-id="2ca53-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-469">WiaItemTypeStorage</span><span class="sxs-lookup"><span data-stu-id="2ca53-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="2ca53-470">此旗標表示資料夾專案的額外儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2ca53-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="2ca53-471">WIA 驅動程式會根據影像和資料夾來指定其專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="2ca53-472">沒有任何 WIA 屬性描述儲存專案的特性 (例如剩餘的儲存空間、寫入速度或媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2ca53-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="2ca53-473">您可以新增可公開此資訊的廠商特定屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="2ca53-474">這些屬性只能存取為了辨識這些屬性而撰寫的應用程式或延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2ca53-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-475">WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="2ca53-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="2ca53-476">這個專案可以用來傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="2ca53-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-477">WiaItemTypeTwainCapabilityPassThrough</span><span class="sxs-lookup"><span data-stu-id="2ca53-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="2ca53-478">這種類型表示 WIA 裝置能夠接收來自 TWAIN 相容性層的 TWAIN 功能資料。</span><span class="sxs-lookup"><span data-stu-id="2ca53-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="2ca53-479">如果設定此型別，則 TWAIN 相容性層所不了解的任何 TWAIN 功能都會傳遞至 theWIA 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="2ca53-480">這僅適用于根項目。</span><span class="sxs-lookup"><span data-stu-id="2ca53-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-481">WiaItemTypeVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="2ca53-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="2ca53-482">此專案支援串流處理影片。</span><span class="sxs-lookup"><span data-stu-id="2ca53-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-483">WiaItemTypeVPanorama\*</span><span class="sxs-lookup"><span data-stu-id="2ca53-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="2ca53-484">此專案代表垂直全景影像。</span><span class="sxs-lookup"><span data-stu-id="2ca53-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="2ca53-485">此旗標只適用于也已設定 <strong>WiaItemTypeFolder</strong> 旗標的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2ca53-486">根據專案的類別，這些旗標中有些旗標是必要或選擇性2.0 的，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="2ca53-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-487">專案類別</span><span class="sxs-lookup"><span data-stu-id="2ca53-487">Category of Item</span></span></th>
<th><span data-ttu-id="2ca53-488">必要</span><span class="sxs-lookup"><span data-stu-id="2ca53-488">Required</span></span></th>
<th><span data-ttu-id="2ca53-489">選用</span><span class="sxs-lookup"><span data-stu-id="2ca53-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="2ca53-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="2ca53-491">WiaItemTypeRoot WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="2ca53-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="2ca53-492">WiaItemTypeDevice WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="2ca53-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="2ca53-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="2ca53-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="2ca53-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="2ca53-495">WiaItemTypeFolder (如果支援多個掃描區域專案，此旗標只適用于 WIA_CATEGORY_FLATBED 根專案。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="2ca53-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="2ca53-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="2ca53-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="2ca53-498">WiaItemTypeFolder (如果 WIA_CATEGORY_FEEDER_FRONT 和 WIA_CATEGORY_FEEDER_BACK 專案都存在，則此旗標只適用于 WIA_CATEGORY_FEEDER 根專案。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-499">WIA_CATEGORY_FILM (根) </span><span class="sxs-lookup"><span data-stu-id="2ca53-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="2ca53-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="2ca53-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="2ca53-501">無</span><span class="sxs-lookup"><span data-stu-id="2ca53-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-502">WIA_CATEGORY_FILM (子系) </span><span class="sxs-lookup"><span data-stu-id="2ca53-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="2ca53-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="2ca53-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="2ca53-504">無</span><span class="sxs-lookup"><span data-stu-id="2ca53-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="2ca53-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="2ca53-506">WiaItemTypeStorage WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="2ca53-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="2ca53-507">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="2ca53-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="2ca53-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="2ca53-509">WiaItemTypeFile WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="2ca53-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="2ca53-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="2ca53-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="2ca53-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-512">包含專案名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca53-512">Contains the item name.</span></span> <span data-ttu-id="2ca53-513">應用程式會讀取此屬性，以判斷其目前使用的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="2ca53-514">每個專案都有唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca53-514">Each item has a unique name.</span></span> <span data-ttu-id="2ca53-515">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-516">所有 WIA 2.0 專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-517">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="2ca53-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-519">包含與專案相關聯之資料的目前大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2ca53-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="2ca53-520">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-521">[包含] 是要傳輸的資料大小總計。</span><span class="sxs-lookup"><span data-stu-id="2ca53-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="2ca53-522">如果此值為零，則表示迷你驅動程式沒有資料確切大小的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2ca53-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="2ca53-523"> (這常見於壓縮的資料。 ) 應用程式會讀取此值，以在發生之前判斷取得的大小。</span><span class="sxs-lookup"><span data-stu-id="2ca53-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="2ca53-524">WIA 服務會讀取此屬性，以協助配置記憶體以進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="2ca53-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="2ca53-525">如需詳細資訊，請參閱將 <a href="https://msdn.microsoft.com/library/ms792198.aspx">資料傳送至 WIA 應用程式</a> 。如果屬性設為零，且 TYMED 設定為檔案傳輸，則 wia 服務不會配置任何記憶體給 wia 迷你驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="2ca53-526">所有已啟用轉換的 WIA 2.0 專案都需要。</span><span class="sxs-lookup"><span data-stu-id="2ca53-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-527">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="2ca53-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-529">包含最初捕獲映射的時間。</span><span class="sxs-lookup"><span data-stu-id="2ca53-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="2ca53-530">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="2ca53-531">這個屬性應該以 SYSTEMTIME 結構的形式回報為八個 <strong>單字</strong> 值的向量 (如 Platform SDK 檔) 中所述。</span><span class="sxs-lookup"><span data-stu-id="2ca53-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="2ca53-532">所有 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-533">類型： <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="2ca53-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-535">只有在 Windows Vista 和更新版本中才支援。</span><span class="sxs-lookup"><span data-stu-id="2ca53-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="2ca53-536">指定 WIA_CATEGORY_FOLDER 專案中儲存的專案數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="2ca53-537">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="2ca53-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-539">指定資料傳輸中使用的最小緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2ca53-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="2ca53-540">如果資料傳輸是透過回呼機制來執行，屬性值可以小到64KB。</span><span class="sxs-lookup"><span data-stu-id="2ca53-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="2ca53-541">但是，如果傳送至檔案，屬性值就是一次傳輸一個資料頁面所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2ca53-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="2ca53-542">迷你驅動程式會建立並維護此 WIA 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="2ca53-543">所有已啟用轉換的 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-544">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="2ca53-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-546">包含影像中所含的行數 (影像的垂直高度（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="2ca53-547">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-548">所有 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-549">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="2ca53-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-551">包含影像中每一行的圖元數 (影像的寬度（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="2ca53-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="2ca53-552">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-553">所有 WIA 2.0 專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ca53-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-554">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="2ca53-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-556">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="2ca53-557">包含影像資料封裝選項。</span><span class="sxs-lookup"><span data-stu-id="2ca53-557">Contains image data packing options.</span></span> <span data-ttu-id="2ca53-558">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-559">應用程式會讀取這個屬性，以判斷影像封裝選項，或設定目前的影像封裝選項。</span><span class="sxs-lookup"><span data-stu-id="2ca53-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="2ca53-560">類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>。</span><span class="sxs-lookup"><span data-stu-id="2ca53-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="2ca53-561">如果裝置只能設定為單一值，請建立 WIA_PROP_LIST 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="2ca53-562">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-563">值</span><span class="sxs-lookup"><span data-stu-id="2ca53-563">Value</span></span></th>
<th><span data-ttu-id="2ca53-564">定義</span><span class="sxs-lookup"><span data-stu-id="2ca53-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="2ca53-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="2ca53-566">影像資料採用壓縮的像素格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="2ca53-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="2ca53-568">影像資料是平面格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="2ca53-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-570">包含此迷你驅動程式所傳送影像的慣用格式。</span><span class="sxs-lookup"><span data-stu-id="2ca53-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="2ca53-571">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-572">所有已啟用轉換的 WIA 2.0 專案都需要。</span><span class="sxs-lookup"><span data-stu-id="2ca53-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-573">類型： <strong>CLSID</strong>、Access：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="2ca53-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-575">指定代表一組裝置屬性值的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="2ca53-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="2ca53-576">如果設備磁碟機會執行這項功能，應用程式會使用這個屬性來判斷裝置是否支援一組值。</span><span class="sxs-lookup"><span data-stu-id="2ca53-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="2ca53-577">類型： <strong>CLSID</strong>、Access：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2ca53-578">下表具有12個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-579">值</span><span class="sxs-lookup"><span data-stu-id="2ca53-579">Value</span></span></th>
<th><span data-ttu-id="2ca53-580">定義</span><span class="sxs-lookup"><span data-stu-id="2ca53-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="2ca53-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="2ca53-582">具有標頭檔的 MicrosoftWindows 點陣圖</span><span class="sxs-lookup"><span data-stu-id="2ca53-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="2ca53-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="2ca53-584">擴充的 Windows 中繼檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="2ca53-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="2ca53-586">交換檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="2ca53-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="2ca53-588">FlashPix 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="2ca53-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="2ca53-590">GIF 影像格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="2ca53-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="2ca53-592">Windows 圖示檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="2ca53-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="2ca53-594">JPEG 壓縮格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="2ca53-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="2ca53-596">Eastman Kodak 檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="2ca53-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="2ca53-598">W3C PNG 格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="2ca53-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="2ca53-600">沒有標頭檔的 Windows 點陣圖</span><span class="sxs-lookup"><span data-stu-id="2ca53-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="2ca53-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="2ca53-602">TIF 檔案格式</span><span class="sxs-lookup"><span data-stu-id="2ca53-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="2ca53-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="2ca53-604">Windows 中繼檔</span><span class="sxs-lookup"><span data-stu-id="2ca53-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="2ca53-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-606">只有在 Windows Vista 和更新版本中才支援。</span><span class="sxs-lookup"><span data-stu-id="2ca53-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="2ca53-607">包含每個通道中的位數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="2ca53-608">這個屬性應該回報為多個位元組值的向量（如同通道的數目），其中第一個位元組會對應到第一個通道中的位數，第二個位元組會對應到第二個通道中的位數，依此類推。</span><span class="sxs-lookup"><span data-stu-id="2ca53-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="2ca53-609">根據 WIA_IPA_CHANNELS_PER_PIXEL，每個頻道都必須有任意數量的專案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="2ca53-610">當應用程式切換為 WiaImgFmt_RAW 時，驅動程式會設定該屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="2ca53-611">針對已知的子類型，WIA_IPA_RAW_SUBTYPE 的表格中所列的專案數目如下。</span><span class="sxs-lookup"><span data-stu-id="2ca53-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="2ca53-612">類型： <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="2ca53-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-614">這個屬性是保留供日後使用，且目前不會執行。</span><span class="sxs-lookup"><span data-stu-id="2ca53-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="2ca53-615">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="2ca53-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-617">指定是否要隱藏裝置上專案的一般屬性頁。</span><span class="sxs-lookup"><span data-stu-id="2ca53-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="2ca53-618">這個屬性可在 Windows XP 和更新版本上使用。</span><span class="sxs-lookup"><span data-stu-id="2ca53-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="2ca53-619">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2ca53-620">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="2ca53-621">星號 \* 表示常數在 Windows Vista 和更新版本中是不正確。</span><span class="sxs-lookup"><span data-stu-id="2ca53-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="2ca53-622"> (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-623">常數</span><span class="sxs-lookup"><span data-stu-id="2ca53-623">Constant</span></span></th>
<th><span data-ttu-id="2ca53-624">描述</span><span class="sxs-lookup"><span data-stu-id="2ca53-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="2ca53-626">隱藏相機的一般專案屬性頁。</span><span class="sxs-lookup"><span data-stu-id="2ca53-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="2ca53-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="2ca53-628">隱藏掃描器的一般專案屬性頁。</span><span class="sxs-lookup"><span data-stu-id="2ca53-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="2ca53-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-630">此屬性包含傳送方法設定。</span><span class="sxs-lookup"><span data-stu-id="2ca53-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="2ca53-631">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca53-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2ca53-632">應用程式會讀取這個屬性，以判斷迷你驅動程式的資料傳輸方法。</span><span class="sxs-lookup"><span data-stu-id="2ca53-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="2ca53-633">所有已啟用轉換的 WIA 2.0 專案都需要。</span><span class="sxs-lookup"><span data-stu-id="2ca53-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="2ca53-634">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2ca53-635">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="2ca53-636">星號 \* 表示在 Windows Vista 和更新版本中不正確常數。</span><span class="sxs-lookup"><span data-stu-id="2ca53-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="2ca53-637"> (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) </span><span class="sxs-lookup"><span data-stu-id="2ca53-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca53-638">類型中的來源</span><span class="sxs-lookup"><span data-stu-id="2ca53-638">Transfer Type</span></span></th>
<th><span data-ttu-id="2ca53-639">Description</span><span class="sxs-lookup"><span data-stu-id="2ca53-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca53-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="2ca53-641">將影像傳送至記憶體（以群組區）。</span><span class="sxs-lookup"><span data-stu-id="2ca53-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="2ca53-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="2ca53-643">將多個映射傳送至記憶體（以群組區為限）。</span><span class="sxs-lookup"><span data-stu-id="2ca53-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca53-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="2ca53-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="2ca53-645">將影像傳送至檔案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca53-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="2ca53-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="2ca53-647">將影像傳送至檔案。</span><span class="sxs-lookup"><span data-stu-id="2ca53-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="2ca53-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2ca53-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2ca53-649">只有在 Windows Vista 和更新版本中才支援。</span><span class="sxs-lookup"><span data-stu-id="2ca53-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="2ca53-650">指定要為專案上傳的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2ca53-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="2ca53-651">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2ca53-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="2ca53-652">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ca53-652">Requirements</span></span>



| <span data-ttu-id="2ca53-653">需求</span><span class="sxs-lookup"><span data-stu-id="2ca53-653">Requirement</span></span> | <span data-ttu-id="2ca53-654">值</span><span class="sxs-lookup"><span data-stu-id="2ca53-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca53-655">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ca53-655">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca53-656">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ca53-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2ca53-657">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ca53-657">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca53-658">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ca53-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2ca53-659">標頭</span><span class="sxs-lookup"><span data-stu-id="2ca53-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca53-660"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca53-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




