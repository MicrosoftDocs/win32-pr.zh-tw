---
description: DVD 禁止複製屬性集提供從硬體或軟體 decrypters 禁止複製資訊的驗證。 使用這個屬性集，以防止未經授權的 DVD 影片複製。
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD 複製保護屬性集 (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909476"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="ec65d-104">DVD 禁止複製屬性集</span><span class="sxs-lookup"><span data-stu-id="ec65d-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="ec65d-105">DVD 禁止複製屬性集提供從硬體或軟體 decrypters 禁止複製資訊的驗證。</span><span class="sxs-lookup"><span data-stu-id="ec65d-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="ec65d-106">使用這個屬性集，以防止未經授權的 DVD 影片複製。</span><span class="sxs-lookup"><span data-stu-id="ec65d-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="ec65d-107">Microsoft 提供的軟體可協助加密配置所需的驗證程式，因此可讓 DVD-ROM 光碟機以 DVD decrypter 來驗證和傳輸金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec65d-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="ec65d-108">Microsoft 目前沒有計劃寄送 DVD decrypter，而是提供作業系統程式碼，作為代理程式來啟用硬體或軟體 decrypters 的驗證。</span><span class="sxs-lookup"><span data-stu-id="ec65d-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="ec65d-109">DVD 導覽器會初始化並控制金鑰交換程式。</span><span class="sxs-lookup"><span data-stu-id="ec65d-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="ec65d-110">DVD 迷你驅動程式只需要執行下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="ec65d-111">其他元件則會處理其餘部分。</span><span class="sxs-lookup"><span data-stu-id="ec65d-111">Other components handle the rest.</span></span>

<span data-ttu-id="ec65d-112">每個 DVD 輸入串流都會接收禁止複製屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="ec65d-113">即使相同硬體控制所有 DVD 串流，也是如此。</span><span class="sxs-lookup"><span data-stu-id="ec65d-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="ec65d-114">下列資訊提供在呼叫 [**IKsPropertySet**](ikspropertyset.md) 方法時，要用於此屬性集的必要常數和資料類型。</span><span class="sxs-lookup"><span data-stu-id="ec65d-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="ec65d-115">它會提供 **GUID** (*GuidPropSet*) 、屬性識別碼 (*dwPropID*) 和屬性資料類型的值， (*pPropData*) 參數。</span><span class="sxs-lookup"><span data-stu-id="ec65d-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="ec65d-116">標籤</span><span class="sxs-lookup"><span data-stu-id="ec65d-116">Label</span></span> | <span data-ttu-id="ec65d-117">值</span><span class="sxs-lookup"><span data-stu-id="ec65d-117">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="ec65d-118">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="ec65d-118">Property Set GUID</span></span> | <span data-ttu-id="ec65d-119">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="ec65d-119">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec65d-120">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="ec65d-120">Property ID</span></span></th>
<th><span data-ttu-id="ec65d-121">描述</span><span class="sxs-lookup"><span data-stu-id="ec65d-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec65d-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec65d-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="ec65d-123">查詢影片輸出是否為標準定義、類比元件影片。</span><span class="sxs-lookup"><span data-stu-id="ec65d-123">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec65d-124">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="ec65d-124">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="ec65d-125">這是僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-125">This is a set-only property.</span></span> <span data-ttu-id="ec65d-126">這個屬性會在接收 pin 的輸出結尾設定 NTSC 編碼器的類比禁止複製層級。</span><span class="sxs-lookup"><span data-stu-id="ec65d-126">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="ec65d-127">使用 <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="ec65d-127">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec65d-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="ec65d-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="ec65d-129">這個屬性支援 get 和 set 作業。</span><span class="sxs-lookup"><span data-stu-id="ec65d-129">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="ec65d-130">Get 作業會要求解碼器提供其匯流排挑戰金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec65d-130">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="ec65d-131">設定作業會提供具有來自 DVD 光碟機之匯流排挑戰金鑰的解碼器。</span><span class="sxs-lookup"><span data-stu-id="ec65d-131">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="ec65d-132">在這個屬性中傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-132">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec65d-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="ec65d-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="ec65d-134">這是僅供取得的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-134">This is a get-only property.</span></span> <span data-ttu-id="ec65d-135">這個屬性會要求將解碼器的匯流排金鑰2傳輸到 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="ec65d-135">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="ec65d-136">傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-136">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec65d-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="ec65d-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="ec65d-138">僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-138">Set-only property.</span></span> <span data-ttu-id="ec65d-139">這會提供光碟機碼。</span><span class="sxs-lookup"><span data-stu-id="ec65d-139">This provides disc key.</span></span> <span data-ttu-id="ec65d-140">索引鍵是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-140">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec65d-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="ec65d-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="ec65d-142">這是僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-142">This is a set-only property.</span></span> <span data-ttu-id="ec65d-143">這個屬性會將 DVD 磁片磁碟機匯流排金鑰1提供給解碼器。</span><span class="sxs-lookup"><span data-stu-id="ec65d-143">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="ec65d-144">傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-144">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec65d-145">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="ec65d-145">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="ec65d-146">區域程式碼會要求使用此解碼器的區域定義，如 DVD 協會所定義。</span><span class="sxs-lookup"><span data-stu-id="ec65d-146">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="ec65d-147">此區域定義為 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-147">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec65d-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="ec65d-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="ec65d-149">Get 和 set 都支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-149">Both get and set are supported on this property.</span></span> <span data-ttu-id="ec65d-150">首先會呼叫 Get，以判斷是否需要驗證。</span><span class="sxs-lookup"><span data-stu-id="ec65d-150">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="ec65d-151">設定的屬性會指出篩選所輸入的禁止複製協調階段。</span><span class="sxs-lookup"><span data-stu-id="ec65d-151">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="ec65d-152">傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-152">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec65d-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="ec65d-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="ec65d-154">如果這個屬性為 <strong>TRUE</strong>，則在協商光碟機碼之前，DVD 導覽器不會傳送 <strong>AM_UseNewCSSKey</strong> 範例。</span><span class="sxs-lookup"><span data-stu-id="ec65d-154">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="ec65d-155">請參閱 <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="ec65d-155">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="ec65d-156">唯讀。</span><span class="sxs-lookup"><span data-stu-id="ec65d-156">Read-only.</span></span> <span data-ttu-id="ec65d-157">屬性資料是 <strong>布林</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="ec65d-157">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ec65d-158">適用于 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="ec65d-158">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec65d-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="ec65d-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="ec65d-160">這是僅限設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65d-160">This is a set-only property.</span></span> <span data-ttu-id="ec65d-161">這會從目前內容提供標題索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ec65d-161">This provides title key from current content.</span></span> <span data-ttu-id="ec65d-162">索引鍵是 <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>類型的結構。</span><span class="sxs-lookup"><span data-stu-id="ec65d-162">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="ec65d-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec65d-163">Requirements</span></span>



| <span data-ttu-id="ec65d-164">需求</span><span class="sxs-lookup"><span data-stu-id="ec65d-164">Requirement</span></span> | <span data-ttu-id="ec65d-165">值</span><span class="sxs-lookup"><span data-stu-id="ec65d-165">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec65d-166">標頭</span><span class="sxs-lookup"><span data-stu-id="ec65d-166">Header</span></span><br/> | <dl> <span data-ttu-id="ec65d-167"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec65d-167"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec65d-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec65d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec65d-169">屬性集</span><span class="sxs-lookup"><span data-stu-id="ec65d-169">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




