---
title: 'DRM_LICENSE_STATE_DATA 結構 (Drmexternals .h) '
description: DRM \_ 授權 \_ 狀態 \_ 資料結構包含有關指定之 DRM 許可權的授權資訊。
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969604"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="56118-105">DRM_LICENSE_STATE_DATA 結構 (Drmexternals .h) </span><span class="sxs-lookup"><span data-stu-id="56118-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="56118-106">**Drm \_ 授權 \_ 狀態 \_ 資料** 結構包含有關指定之 [*DRM*](wmformat-glossary.md)許可權的 [*授權*](wmformat-glossary.md)資訊。</span><span class="sxs-lookup"><span data-stu-id="56118-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="56118-107">語法</span><span class="sxs-lookup"><span data-stu-id="56118-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="56118-108">成員</span><span class="sxs-lookup"><span data-stu-id="56118-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="56118-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="56118-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="56118-110">要套用授權的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="56118-110">Stream number to which the license applies.</span></span> <span data-ttu-id="56118-111">必須是0，表示授權會套用至檔案中的所有資料流程。</span><span class="sxs-lookup"><span data-stu-id="56118-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="56118-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="56118-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="56118-113">要顯示的字串類別。</span><span class="sxs-lookup"><span data-stu-id="56118-113">Category of string to be displayed.</span></span> <span data-ttu-id="56118-114">如需可能的值及其意義，請參閱 [**DRM \_ 授權 \_ 狀態 \_ 類別目錄**](drm-license-state-category.md) 。</span><span class="sxs-lookup"><span data-stu-id="56118-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="56118-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="56118-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="56118-116">**DwCount** 中提供的專案數。</span><span class="sxs-lookup"><span data-stu-id="56118-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="56118-117">此值通常是0或1。</span><span class="sxs-lookup"><span data-stu-id="56118-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="56118-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="56118-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="56118-119">0或1或更多 **DWORD** 的陣列，代表在 **dwCategory** 中指定的動作可能執行的次數。</span><span class="sxs-lookup"><span data-stu-id="56118-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="56118-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="56118-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="56118-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="56118-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="56118-122">**Datetime** 中提供的專案數。</span><span class="sxs-lookup"><span data-stu-id="56118-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="56118-123">通常不會使用兩個以上的日期，例如，具有從一個日期起生效的授權，直到另一個日期為止。</span><span class="sxs-lookup"><span data-stu-id="56118-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="56118-124">**日期時間 \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="56118-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="56118-125">一或多個 FILETIME 結構的陣列，代表授權中的一或多個日期。</span><span class="sxs-lookup"><span data-stu-id="56118-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="56118-126">特定日期的意義取決於 **dwCategory** 的值。</span><span class="sxs-lookup"><span data-stu-id="56118-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="56118-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="56118-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="56118-128">下列的零或多個旗標與位 **or** 結合：</span><span class="sxs-lookup"><span data-stu-id="56118-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="56118-129">旗標</span><span class="sxs-lookup"><span data-stu-id="56118-129">Flag</span></span>                                    | <span data-ttu-id="56118-130">描述</span><span class="sxs-lookup"><span data-stu-id="56118-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56118-131">DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊</span><span class="sxs-lookup"><span data-stu-id="56118-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="56118-132">如果設定，則可能會有更多適用于內容的授權。</span><span class="sxs-lookup"><span data-stu-id="56118-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="56118-133">DRM \_ 授權 \_ 狀態 \_ 資料 \_ OPL \_ 存在</span><span class="sxs-lookup"><span data-stu-id="56118-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="56118-134">如果設定，授權就會包含輸出保護層級 (OPLs) 必須針對應用程式輸出的目的地進行抓取和檢查。</span><span class="sxs-lookup"><span data-stu-id="56118-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="56118-135">\_提供 SAP 的 DRM 授權 \_ 狀態 \_ 資料 \_ \_</span><span class="sxs-lookup"><span data-stu-id="56118-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="56118-136">如果設定，則必須使用 (SAP) 的安全音訊路徑來傳遞內容。</span><span class="sxs-lookup"><span data-stu-id="56118-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56118-137">備註</span><span class="sxs-lookup"><span data-stu-id="56118-137">Remarks</span></span>

<span data-ttu-id="56118-138">當您指定其中一個 DRM 授權狀態屬性時，會從 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)的呼叫，將此結構傳回 (封裝于 [**WM \_ 授權 \_ 狀態 \_ 資料**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))結構) 。</span><span class="sxs-lookup"><span data-stu-id="56118-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="56118-139">這些屬性是：</span><span class="sxs-lookup"><span data-stu-id="56118-139">These properties are:</span></span>

-   [<span data-ttu-id="56118-140">**DRM \_ LicenseState \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="56118-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="56118-141">**DRM \_ LicenseState \_ CopyToCD**</span><span class="sxs-lookup"><span data-stu-id="56118-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="56118-142">**DRM \_ LicenseState \_ CopyToSDMIDevice**</span><span class="sxs-lookup"><span data-stu-id="56118-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="56118-143">**DRM \_ LicenseState \_ CopyToNonSDMIDevice**</span><span class="sxs-lookup"><span data-stu-id="56118-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="56118-144">**DRM \_ LicenseState \_ CollaborativePlay**</span><span class="sxs-lookup"><span data-stu-id="56118-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="56118-145">**DRM \_ LicenseState \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="56118-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="56118-146">**DRM \_ LicenseState \_ PlaylistBurn**</span><span class="sxs-lookup"><span data-stu-id="56118-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="56118-147">如果 **dwCategory** 是 **\_ 從 UNTIL 起算的 WM DRM \_ 授權 \_ 狀態 \_ 計數 \_ \_ ，** 則 **日期時間** 陣列通常會包含兩個日期： "FROM" 日期和 "UNTIL" 日期。</span><span class="sxs-lookup"><span data-stu-id="56118-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="56118-148">也可以指定兩個日期組來建立更複雜的授權。</span><span class="sxs-lookup"><span data-stu-id="56118-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="56118-149">**DwCount** 陣列的元素會對應至 **datetime** 陣列中所指定的日期或日期範圍。</span><span class="sxs-lookup"><span data-stu-id="56118-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="56118-150">如果 **dwCategory** 是 **從到 datetime 的 WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ \_** ，且 **datetime** 包含一對日期，則 **dwCount** 將會包含一個專案。</span><span class="sxs-lookup"><span data-stu-id="56118-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="56118-151">如果日期 **時間** 包含兩個日期組 (四個元素) ，則 **dwCount** 應該包含兩個元素，每個日期組各一個專案。</span><span class="sxs-lookup"><span data-stu-id="56118-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="56118-152">在某些情況下，使用者可能會被發給一個以上的檔案授權。</span><span class="sxs-lookup"><span data-stu-id="56118-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="56118-153">例如，他們可能已取得允許五個播放的授權，直到當月結束為止，並于稍後取得無限制許可權的第二個授權。</span><span class="sxs-lookup"><span data-stu-id="56118-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="56118-154">在這種情況下，DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊旗標會設定在 **dwVague** () 中， `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` 而 drm 元件會使用演算法來判斷最可能套用的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="56118-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="56118-155">當某個授權到期時，DRM 元件將會檢查剩餘的授權 (s) ，依此類推，直到所有授權都過期為止。</span><span class="sxs-lookup"><span data-stu-id="56118-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="56118-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="56118-156">Requirements</span></span>



| <span data-ttu-id="56118-157">需求</span><span class="sxs-lookup"><span data-stu-id="56118-157">Requirement</span></span> | <span data-ttu-id="56118-158">值</span><span class="sxs-lookup"><span data-stu-id="56118-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="56118-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56118-159">Minimum supported client</span></span><br/> | <span data-ttu-id="56118-160">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56118-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="56118-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56118-161">Minimum supported server</span></span><br/> | <span data-ttu-id="56118-162">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56118-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="56118-163">版本</span><span class="sxs-lookup"><span data-stu-id="56118-163">Version</span></span><br/>                  | <span data-ttu-id="56118-164">Windows Media Format 7 SDK 或更新版本的 SDK</span><span class="sxs-lookup"><span data-stu-id="56118-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="56118-165">標頭</span><span class="sxs-lookup"><span data-stu-id="56118-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="56118-166"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="56118-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56118-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56118-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56118-168">**結構**</span><span class="sxs-lookup"><span data-stu-id="56118-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

