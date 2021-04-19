---
title: 'DRM_LICENSE_STATE_DATA 結構 (Wmdrmsdk .h) '
description: DRM \_ 授權 \_ 狀態 \_ 資料結構包含 drm 許可權的授許可權制相關資訊。
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999633"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="76f4d-105">DRM_LICENSE_STATE_DATA 結構 (Wmdrmsdk .h) </span><span class="sxs-lookup"><span data-stu-id="76f4d-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="76f4d-106">**Drm \_ 授權 \_ 狀態 \_ 資料** 結構包含 drm 許可權的授許可權制相關資訊。</span><span class="sxs-lookup"><span data-stu-id="76f4d-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f4d-107">語法</span><span class="sxs-lookup"><span data-stu-id="76f4d-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="76f4d-108">成員</span><span class="sxs-lookup"><span data-stu-id="76f4d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="76f4d-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="76f4d-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-110">要套用授權的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="76f4d-110">Stream number to which the license applies.</span></span> <span data-ttu-id="76f4d-111">必須是0，表示授權會套用至檔案中的所有資料流程。</span><span class="sxs-lookup"><span data-stu-id="76f4d-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="76f4d-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="76f4d-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-113">要顯示的字串類別。</span><span class="sxs-lookup"><span data-stu-id="76f4d-113">Category of string to be displayed.</span></span> <span data-ttu-id="76f4d-114">如需可能的值及其意義，請參閱 [**DRM \_ 授權 \_ 狀態 \_ 類別目錄**](drmdrm-license-state-category.md) 。</span><span class="sxs-lookup"><span data-stu-id="76f4d-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="76f4d-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="76f4d-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-116">**DwCount** 中提供的專案數。</span><span class="sxs-lookup"><span data-stu-id="76f4d-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="76f4d-117">此值通常是0或1。</span><span class="sxs-lookup"><span data-stu-id="76f4d-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="76f4d-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="76f4d-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-119">0或1或更多 **DWORD** 值的陣列，代表可執行 **dwCategory** 中指定之動作的次數。</span><span class="sxs-lookup"><span data-stu-id="76f4d-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="76f4d-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="76f4d-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76f4d-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="76f4d-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-122">**Datetime** 中提供的專案數。</span><span class="sxs-lookup"><span data-stu-id="76f4d-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="76f4d-123">通常不會使用兩個以上的日期，例如，具有從一個日期起生效的授權，直到另一個日期為止。</span><span class="sxs-lookup"><span data-stu-id="76f4d-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="76f4d-124">**日期時間 \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="76f4d-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-125">一或多個 **FILETIME** 結構的陣列，代表授權中的一或多個日期。</span><span class="sxs-lookup"><span data-stu-id="76f4d-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="76f4d-126">特定日期的意義取決於 **dwCategory** 的值。</span><span class="sxs-lookup"><span data-stu-id="76f4d-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="76f4d-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="76f4d-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="76f4d-128">下列的零或多個旗標與位 **or** 結合：</span><span class="sxs-lookup"><span data-stu-id="76f4d-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="76f4d-129">旗標</span><span class="sxs-lookup"><span data-stu-id="76f4d-129">Flag</span></span>                                    | <span data-ttu-id="76f4d-130">描述</span><span class="sxs-lookup"><span data-stu-id="76f4d-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76f4d-131">DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊</span><span class="sxs-lookup"><span data-stu-id="76f4d-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="76f4d-132">如果設定，則可能會有更多適用于內容的授權。</span><span class="sxs-lookup"><span data-stu-id="76f4d-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="76f4d-133">要確定適用于指定金鑰識別碼之個別授權的唯一方法是列舉授權。</span><span class="sxs-lookup"><span data-stu-id="76f4d-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="76f4d-134">若要這樣做，請呼叫 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)，並傳遞金鑰識別碼作為 bstrKID 參數。</span><span class="sxs-lookup"><span data-stu-id="76f4d-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="76f4d-135">然後使用已取出的 IWMDRMLicense 介面來檢查授權。</span><span class="sxs-lookup"><span data-stu-id="76f4d-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="76f4d-136">DRM \_ 授權 \_ 狀態 \_ 資料 \_ OPL \_ 存在</span><span class="sxs-lookup"><span data-stu-id="76f4d-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="76f4d-137">如果設定，授權就會包含輸出保護層級 (OPLs) 必須針對應用程式輸出的目的地進行抓取和檢查。</span><span class="sxs-lookup"><span data-stu-id="76f4d-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="76f4d-138">\_提供 SAP 的 DRM 授權 \_ 狀態 \_ 資料 \_ \_</span><span class="sxs-lookup"><span data-stu-id="76f4d-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="76f4d-139">如果設定，則必須使用 (SAP) 的安全音訊路徑來傳遞內容。</span><span class="sxs-lookup"><span data-stu-id="76f4d-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76f4d-140">備註</span><span class="sxs-lookup"><span data-stu-id="76f4d-140">Remarks</span></span>

<span data-ttu-id="76f4d-141">藉由呼叫 **IWMDRMLicenseQuery：： QueryLicenseState**，即可取出此結構。</span><span class="sxs-lookup"><span data-stu-id="76f4d-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="76f4d-142">如果 **dwCategory** 是 **\_ \_ \_ \_ \_ 從 \_ UNTIL 起算的 WM DRM 授權狀態計數**，則 **日期時間** 陣列通常會包含兩個日期： "FROM" 日期和 "UNTIL" 日期。</span><span class="sxs-lookup"><span data-stu-id="76f4d-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="76f4d-143">也可以指定兩個日期組來建立更複雜的授權。</span><span class="sxs-lookup"><span data-stu-id="76f4d-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="76f4d-144">**DwCount** 陣列的元素會對應至 **datetime** 陣列中所指定的日期或日期範圍。</span><span class="sxs-lookup"><span data-stu-id="76f4d-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="76f4d-145">如果 **dwCategory** 是 **從到 datetime 的 WM \_ DRM \_ 授權 \_ 狀態 \_ 計數 \_ \_** ，且 **datetime** 包含一對日期，則 **dwCount** 將會包含一個專案。</span><span class="sxs-lookup"><span data-stu-id="76f4d-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="76f4d-146">如果日期 **時間** 包含兩個日期組 (四個元素) ，則 **dwCount** 應該包含兩個元素，每個日期組各一個專案。</span><span class="sxs-lookup"><span data-stu-id="76f4d-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="76f4d-147">在某些情況下，使用者可能會被發給一個以上的檔案授權。</span><span class="sxs-lookup"><span data-stu-id="76f4d-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="76f4d-148">例如，他們可能已取得允許五個播放的授權，直到當月結束為止，並于稍後取得無限制許可權的第二個授權。</span><span class="sxs-lookup"><span data-stu-id="76f4d-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="76f4d-149">在這種情況下，DRM \_ 授權 \_ 狀態 \_ 資料 \_ 模糊旗標會設定在 **dwVague** () 中， `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` 而 drm 元件會使用演算法來判斷最可能套用的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="76f4d-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="76f4d-150">當某個授權到期時，DRM 元件將會檢查剩餘的授權，依此類推，直到所有授權都過期為止。</span><span class="sxs-lookup"><span data-stu-id="76f4d-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f4d-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="76f4d-151">Requirements</span></span>



| <span data-ttu-id="76f4d-152">需求</span><span class="sxs-lookup"><span data-stu-id="76f4d-152">Requirement</span></span> | <span data-ttu-id="76f4d-153">值</span><span class="sxs-lookup"><span data-stu-id="76f4d-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76f4d-154">標頭</span><span class="sxs-lookup"><span data-stu-id="76f4d-154">Header</span></span><br/> | <dl> <span data-ttu-id="76f4d-155"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="76f4d-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f4d-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76f4d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f4d-157">**結構**</span><span class="sxs-lookup"><span data-stu-id="76f4d-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





