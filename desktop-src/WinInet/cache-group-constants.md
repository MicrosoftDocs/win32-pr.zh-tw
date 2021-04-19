---
title: '快取群組常數 (Wininet. h) '
description: 下列清單包含快取群組函數所使用的常數。
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967755"
---
# <a name="cache-group-constants"></a><span data-ttu-id="07d37-103">快取群組常數</span><span class="sxs-lookup"><span data-stu-id="07d37-103">Cache Group Constants</span></span>

<span data-ttu-id="07d37-104">下列清單包含快取群組函數所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="07d37-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="07d37-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP \_ 屬性 \_ 基本**</span><span class="sxs-lookup"><span data-stu-id="07d37-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="07d37-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="07d37-107">抓取快取群組的旗標、類型和磁片配額屬性。</span><span class="sxs-lookup"><span data-stu-id="07d37-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="07d37-108">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP \_ 屬性 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="07d37-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="07d37-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="07d37-111">設定或抓取與快取群組相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="07d37-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="07d37-112">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP \_ 屬性 \_ 取得 \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="07d37-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-114">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="07d37-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="07d37-115">抓取快取群組的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="07d37-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="07d37-116">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP \_ 屬性的屬性 \_**</span><span class="sxs-lookup"><span data-stu-id="07d37-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="07d37-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="07d37-119">設定或抓取快取群組的組名。</span><span class="sxs-lookup"><span data-stu-id="07d37-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="07d37-120">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP \_ 屬性 \_ 配額**</span><span class="sxs-lookup"><span data-stu-id="07d37-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="07d37-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="07d37-123">設定或抓取與快取群組相關聯的磁片配額。</span><span class="sxs-lookup"><span data-stu-id="07d37-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="07d37-124">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP \_ 屬性 \_ 儲存體**</span><span class="sxs-lookup"><span data-stu-id="07d37-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="07d37-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="07d37-127">設定或抓取與快取群組相關聯的群組擁有者儲存體。</span><span class="sxs-lookup"><span data-stu-id="07d37-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="07d37-128">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP \_ 屬性 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="07d37-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="07d37-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="07d37-131">設定或抓取快取群組類型。</span><span class="sxs-lookup"><span data-stu-id="07d37-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="07d37-132">[**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP \_ 旗標 \_ FLUSHURL \_ ONDELETE**</span><span class="sxs-lookup"><span data-stu-id="07d37-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="07d37-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="07d37-135">表示應該刪除與快取群組相關聯的所有快取專案，除非該專案屬於另一個快取群組。</span><span class="sxs-lookup"><span data-stu-id="07d37-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP \_ 旗標 \_ GIDONLY**</span><span class="sxs-lookup"><span data-stu-id="07d37-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="07d37-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="07d37-138">指出函式應該只為快取群組建立唯一的 GROUPID，而不是建立實際的群組。</span><span class="sxs-lookup"><span data-stu-id="07d37-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP \_ 旗標 \_ NONPURGEABLE**</span><span class="sxs-lookup"><span data-stu-id="07d37-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="07d37-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="07d37-141">表示無法清除快取群組。</span><span class="sxs-lookup"><span data-stu-id="07d37-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP \_ READWRITE \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="07d37-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="07d37-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="07d37-144">設定快取群組的類型、磁片配額、組名和擁有者儲存體屬性。</span><span class="sxs-lookup"><span data-stu-id="07d37-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="07d37-145">[**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="07d37-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ 搜尋 \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="07d37-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07d37-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="07d37-148">表示應該列舉使用者系統中的所有快取群組。</span><span class="sxs-lookup"><span data-stu-id="07d37-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ 搜尋 \_ BYURL**</span><span class="sxs-lookup"><span data-stu-id="07d37-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="07d37-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="07d37-151">目前未實作。</span><span class="sxs-lookup"><span data-stu-id="07d37-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP \_ 類型 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="07d37-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="07d37-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="07d37-154">指出快取群組類型無效。</span><span class="sxs-lookup"><span data-stu-id="07d37-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**群組 \_ 擁有者 \_ 儲存體 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="07d37-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="07d37-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="07d37-157">群組擁有者儲存陣列的長度。</span><span class="sxs-lookup"><span data-stu-id="07d37-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07d37-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**具有 \_ 最大長度的各名 \_**</span><span class="sxs-lookup"><span data-stu-id="07d37-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="07d37-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="07d37-160">快取組名允許的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="07d37-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07d37-161">備註</span><span class="sxs-lookup"><span data-stu-id="07d37-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="07d37-162">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="07d37-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="07d37-163">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="07d37-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="07d37-164">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="07d37-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07d37-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="07d37-165">Requirements</span></span>



| <span data-ttu-id="07d37-166">需求</span><span class="sxs-lookup"><span data-stu-id="07d37-166">Requirement</span></span> | <span data-ttu-id="07d37-167">值</span><span class="sxs-lookup"><span data-stu-id="07d37-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07d37-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07d37-168">Minimum supported client</span></span><br/> | <span data-ttu-id="07d37-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07d37-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="07d37-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07d37-170">Minimum supported server</span></span><br/> | <span data-ttu-id="07d37-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07d37-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="07d37-172">標頭</span><span class="sxs-lookup"><span data-stu-id="07d37-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d37-173"><dt>Wininet</dt></span><span class="sxs-lookup"><span data-stu-id="07d37-173"><dt>Wininet.h</dt></span></span> </dl> |



 

