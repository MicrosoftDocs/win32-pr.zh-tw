---
description: DVD 禁止複製屬性集提供從硬體或軟體 decrypters 禁止複製資訊的驗證。 使用這個屬性集，以防止未經授權的 DVD 影片複製。
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD 複製保護屬性集 (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991166"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="08cc8-104">DVD 禁止複製屬性集</span><span class="sxs-lookup"><span data-stu-id="08cc8-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="08cc8-105">DVD 禁止複製屬性集提供從硬體或軟體 decrypters 禁止複製資訊的驗證。</span><span class="sxs-lookup"><span data-stu-id="08cc8-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="08cc8-106">使用這個屬性集，以防止未經授權的 DVD 影片複製。</span><span class="sxs-lookup"><span data-stu-id="08cc8-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="08cc8-107">Microsoft 提供的軟體可協助加密配置所需的驗證程式，因此可讓 DVD-ROM 光碟機以 DVD decrypter 來驗證和傳輸金鑰。</span><span class="sxs-lookup"><span data-stu-id="08cc8-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="08cc8-108">Microsoft 目前沒有計劃寄送 DVD decrypter，而是提供作業系統程式碼，作為代理程式來啟用硬體或軟體 decrypters 的驗證。</span><span class="sxs-lookup"><span data-stu-id="08cc8-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="08cc8-109">DVD 導覽器會初始化並控制金鑰交換程式。</span><span class="sxs-lookup"><span data-stu-id="08cc8-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="08cc8-110">DVD 迷你驅動程式只需要執行下列屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="08cc8-111">其他元件則會處理其餘部分。</span><span class="sxs-lookup"><span data-stu-id="08cc8-111">Other components handle the rest.</span></span>

<span data-ttu-id="08cc8-112">每個 DVD 輸入串流都會接收禁止複製屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="08cc8-113">即使相同硬體控制所有 DVD 串流，也是如此。</span><span class="sxs-lookup"><span data-stu-id="08cc8-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="08cc8-114">下列資訊提供在呼叫 [**IKsPropertySet**](ikspropertyset.md) 方法時，要用於此屬性集的必要常數和資料類型。</span><span class="sxs-lookup"><span data-stu-id="08cc8-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="08cc8-115">它會提供 **GUID** (*GuidPropSet*) 、屬性識別碼 (*dwPropID*) 和屬性資料類型的值， (*pPropData*) 參數。</span><span class="sxs-lookup"><span data-stu-id="08cc8-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="08cc8-116">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="08cc8-116">Property Set GUID</span></span> | <span data-ttu-id="08cc8-117">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="08cc8-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08cc8-118">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="08cc8-118">Property ID</span></span></th>
<th><span data-ttu-id="08cc8-119">描述</span><span class="sxs-lookup"><span data-stu-id="08cc8-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08cc8-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="08cc8-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="08cc8-121">查詢影片輸出是否為標準定義、類比元件影片。</span><span class="sxs-lookup"><span data-stu-id="08cc8-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08cc8-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="08cc8-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="08cc8-123">這是僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-123">This is a set-only property.</span></span> <span data-ttu-id="08cc8-124">這個屬性會在接收 pin 的輸出結尾設定 NTSC 編碼器的類比禁止複製層級。</span><span class="sxs-lookup"><span data-stu-id="08cc8-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="08cc8-125">使用 <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="08cc8-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08cc8-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="08cc8-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="08cc8-127">這個屬性支援 get 和 set 作業。</span><span class="sxs-lookup"><span data-stu-id="08cc8-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="08cc8-128">Get 作業會要求解碼器提供其匯流排挑戰金鑰。</span><span class="sxs-lookup"><span data-stu-id="08cc8-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="08cc8-129">設定作業會提供具有來自 DVD 光碟機之匯流排挑戰金鑰的解碼器。</span><span class="sxs-lookup"><span data-stu-id="08cc8-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="08cc8-130">在這個屬性中傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08cc8-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="08cc8-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="08cc8-132">這是僅供取得的屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-132">This is a get-only property.</span></span> <span data-ttu-id="08cc8-133">這個屬性會要求將解碼器的匯流排金鑰2傳輸到 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="08cc8-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="08cc8-134">傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08cc8-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="08cc8-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="08cc8-136">僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-136">Set-only property.</span></span> <span data-ttu-id="08cc8-137">這會提供光碟機碼。</span><span class="sxs-lookup"><span data-stu-id="08cc8-137">This provides disc key.</span></span> <span data-ttu-id="08cc8-138">索引鍵是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08cc8-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="08cc8-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="08cc8-140">這是僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-140">This is a set-only property.</span></span> <span data-ttu-id="08cc8-141">這個屬性會將 DVD 磁片磁碟機匯流排金鑰1提供給解碼器。</span><span class="sxs-lookup"><span data-stu-id="08cc8-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="08cc8-142">傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08cc8-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="08cc8-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="08cc8-144">區域程式碼會要求使用此解碼器的區域定義，如 DVD 協會所定義。</span><span class="sxs-lookup"><span data-stu-id="08cc8-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="08cc8-145">此區域定義為 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08cc8-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="08cc8-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="08cc8-147">Get 和 set 都支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="08cc8-148">首先會呼叫 Get，以判斷是否需要驗證。</span><span class="sxs-lookup"><span data-stu-id="08cc8-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="08cc8-149">設定的屬性會指出篩選所輸入的禁止複製協調階段。</span><span class="sxs-lookup"><span data-stu-id="08cc8-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="08cc8-150">傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08cc8-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="08cc8-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="08cc8-152">如果這個屬性為 <strong>TRUE</strong>，則在協商光碟機碼之前，DVD 導覽器不會傳送 <strong>AM_UseNewCSSKey</strong> 範例。</span><span class="sxs-lookup"><span data-stu-id="08cc8-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="08cc8-153">請參閱 <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="08cc8-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="08cc8-154">唯讀。</span><span class="sxs-lookup"><span data-stu-id="08cc8-154">Read-only.</span></span> <span data-ttu-id="08cc8-155">屬性資料是 <strong>布林</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="08cc8-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08cc8-156">適用于 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="08cc8-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08cc8-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="08cc8-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="08cc8-158">這是僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="08cc8-158">This is a set-only property.</span></span> <span data-ttu-id="08cc8-159">這會從目前內容提供標題索引鍵。</span><span class="sxs-lookup"><span data-stu-id="08cc8-159">This provides title key from current content.</span></span> <span data-ttu-id="08cc8-160">索引鍵是 <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="08cc8-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="08cc8-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="08cc8-161">Requirements</span></span>



| <span data-ttu-id="08cc8-162">需求</span><span class="sxs-lookup"><span data-stu-id="08cc8-162">Requirement</span></span> | <span data-ttu-id="08cc8-163">值</span><span class="sxs-lookup"><span data-stu-id="08cc8-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08cc8-164">標頭</span><span class="sxs-lookup"><span data-stu-id="08cc8-164">Header</span></span><br/> | <dl> <span data-ttu-id="08cc8-165"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="08cc8-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08cc8-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08cc8-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08cc8-167">屬性集</span><span class="sxs-lookup"><span data-stu-id="08cc8-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




