---
title: 'IP_SPECIFIC_DATA 結構 (Rtm) '
description: IP \_ 特定的資料結構包含 ip 特定的資料。
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA 結構 RAS
- PIP_SPECIFIC_DATA 結構指標 RAS
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104676"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="72b14-105">IP \_ 特定的 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="72b14-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="72b14-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="72b14-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="72b14-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="72b14-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="72b14-108">**Ip \_ 特定的資料** 結構包含 ip 特定的資料。</span><span class="sxs-lookup"><span data-stu-id="72b14-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b14-109">語法</span><span class="sxs-lookup"><span data-stu-id="72b14-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="72b14-110">成員</span><span class="sxs-lookup"><span data-stu-id="72b14-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="72b14-111">**FSD \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="72b14-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-112">指定在 [RFC 1354](routing-protocols-request-for-comments.md)中定義的路由類型。</span><span class="sxs-lookup"><span data-stu-id="72b14-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="72b14-113">下表顯示這個成員的可能值。</span><span class="sxs-lookup"><span data-stu-id="72b14-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="72b14-114">成員</span><span class="sxs-lookup"><span data-stu-id="72b14-114">Member</span></span>                                                                                               | <span data-ttu-id="72b14-115">意義</span><span class="sxs-lookup"><span data-stu-id="72b14-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="72b14-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="72b14-117">未指定路由類型。</span><span class="sxs-lookup"><span data-stu-id="72b14-117">The route type is not specified.</span></span> <span data-ttu-id="72b14-118">此類型與此處所列的類型不同。</span><span class="sxs-lookup"><span data-stu-id="72b14-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="72b14-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="72b14-120">路由無效。</span><span class="sxs-lookup"><span data-stu-id="72b14-120">The route is invalid.</span></span> <span data-ttu-id="72b14-121">通常，這個值會用來使路由失效。</span><span class="sxs-lookup"><span data-stu-id="72b14-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="72b14-122">不過，由於路由表管理員不支援失效，因此路由仍會被視為最佳路由計算。</span><span class="sxs-lookup"><span data-stu-id="72b14-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="72b14-123">因此，路由通訊協定不應使用此值。</span><span class="sxs-lookup"><span data-stu-id="72b14-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="72b14-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="72b14-125">路由是本機路由，也就是下一個躍點是最終目的地。</span><span class="sxs-lookup"><span data-stu-id="72b14-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="72b14-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="72b14-127">路由是遠端路由，也就是下一個躍點不是最終目的地。</span><span class="sxs-lookup"><span data-stu-id="72b14-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="72b14-128">**FSD \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="72b14-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-129">指定會導致選取多重路徑路由的一組條件。</span><span class="sxs-lookup"><span data-stu-id="72b14-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="72b14-130">這個成員通常是採用 IP TOS 格式。</span><span class="sxs-lookup"><span data-stu-id="72b14-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="72b14-131">如需詳細資訊，請參閱 [RFC 1354](routing-protocols-request-for-comments.md)。</span><span class="sxs-lookup"><span data-stu-id="72b14-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b14-132">**FSD \_ NextHopAS**</span><span class="sxs-lookup"><span data-stu-id="72b14-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-133">指定下一個躍點的自發系統編號。</span><span class="sxs-lookup"><span data-stu-id="72b14-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="72b14-134">**FSD \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="72b14-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-135">指定度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-135">Specifies a metric value.</span></span> <span data-ttu-id="72b14-136">路由表管理員會使用此值來比較此路由專案與從其他路由通訊協定取得的路由專案。</span><span class="sxs-lookup"><span data-stu-id="72b14-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="72b14-137">此成員的值是由路由表管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="72b14-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="72b14-138">**FSD \_ 度量**</span><span class="sxs-lookup"><span data-stu-id="72b14-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-139">指定度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-139">Specifies a metric value.</span></span> <span data-ttu-id="72b14-140">路由表管理員會使用此值，將此路由專案與從相同路由通訊協定取得的其他路由專案進行比較。</span><span class="sxs-lookup"><span data-stu-id="72b14-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="72b14-141">此成員的值是由路由通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="72b14-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="72b14-142">**FSD \_ Metric1**</span><span class="sxs-lookup"><span data-stu-id="72b14-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-143">指定路由通訊協定特定的度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="72b14-144">此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。</span><span class="sxs-lookup"><span data-stu-id="72b14-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b14-145">**FSD \_ Metric2**</span><span class="sxs-lookup"><span data-stu-id="72b14-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-146">指定路由通訊協定特定的度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="72b14-147">此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。</span><span class="sxs-lookup"><span data-stu-id="72b14-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b14-148">**FSD \_ Metric3**</span><span class="sxs-lookup"><span data-stu-id="72b14-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-149">指定路由通訊協定特定的度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="72b14-150">此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。</span><span class="sxs-lookup"><span data-stu-id="72b14-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b14-151">**FSD \_ Metric4**</span><span class="sxs-lookup"><span data-stu-id="72b14-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-152">指定路由通訊協定特定的度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="72b14-153">此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。</span><span class="sxs-lookup"><span data-stu-id="72b14-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b14-154">**FSD \_ >metric5**</span><span class="sxs-lookup"><span data-stu-id="72b14-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-155">指定路由通訊協定特定的度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="72b14-156">此度量值記載于 [RFC 1354](routing-protocols-request-for-comments.md)中。</span><span class="sxs-lookup"><span data-stu-id="72b14-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b14-157">**FSD \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="72b14-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="72b14-158">指定路由是否有效。</span><span class="sxs-lookup"><span data-stu-id="72b14-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="72b14-159">路由通訊協定應先清除這些旗標，然後將路由設定為有效或無效。</span><span class="sxs-lookup"><span data-stu-id="72b14-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="72b14-160">路由通訊協定應該使用宏 **ClearRouteFlags ()**、 **SetRouteValid ()** 和 **ClearRouteValid ()** 來執行這些作業。</span><span class="sxs-lookup"><span data-stu-id="72b14-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="72b14-161">這些宏是在 Rtm 中定義。</span><span class="sxs-lookup"><span data-stu-id="72b14-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72b14-162">備註</span><span class="sxs-lookup"><span data-stu-id="72b14-162">Remarks</span></span>

<span data-ttu-id="72b14-163">路由表管理員會使用 **FSD \_ Priority** 和 **FSD \_ 計量** 成員，來計算特定目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="72b14-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="72b14-164">**FSD \_ 公制 \[ 1-5 \]** 成員適用于 MIB II 符合規範。</span><span class="sxs-lookup"><span data-stu-id="72b14-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="72b14-165">MIB II 代理程式只會顯示這些度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="72b14-166">它們不會顯示 **FSD 計量 \_** 度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="72b14-167">若要顯示 **FSD \_** 計量，路由通訊協定也應該將值儲存在其中一個 **FSD \_ 公制 \[ 1-5 \]** 成員中。</span><span class="sxs-lookup"><span data-stu-id="72b14-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="72b14-168">路由表管理員在計算目的地網路的最佳路由時，不會使用 **FSD \_ 公制 \[ 1-5 \]** 成員中的計量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="72b14-169">因此，路由通訊協定應確定 FSD 計量 **成員 \_** 具有適當的度量值。</span><span class="sxs-lookup"><span data-stu-id="72b14-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="72b14-170">路由通訊協定可以使用 **FSD \_ 旗** 標，將路由標示為無效（如果其他路由通訊協定不應使用路由）。</span><span class="sxs-lookup"><span data-stu-id="72b14-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b14-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="72b14-171">Requirements</span></span>



| <span data-ttu-id="72b14-172">需求</span><span class="sxs-lookup"><span data-stu-id="72b14-172">Requirement</span></span> | <span data-ttu-id="72b14-173">值</span><span class="sxs-lookup"><span data-stu-id="72b14-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="72b14-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72b14-174">Minimum supported client</span></span><br/> | <span data-ttu-id="72b14-175">都不支援</span><span class="sxs-lookup"><span data-stu-id="72b14-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="72b14-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72b14-176">Minimum supported server</span></span><br/> | <span data-ttu-id="72b14-177">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72b14-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72b14-178">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="72b14-178">End of server support</span></span><br/>    | <span data-ttu-id="72b14-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72b14-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="72b14-180">標頭</span><span class="sxs-lookup"><span data-stu-id="72b14-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b14-181"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b14-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72b14-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b14-183">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="72b14-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="72b14-184">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="72b14-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="72b14-185">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="72b14-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





