---
description: 從載入的捕獲傳回要求的框架。
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: 'ExpertGetFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847742"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="952c7-103">ExpertGetFrame 函式</span><span class="sxs-lookup"><span data-stu-id="952c7-103">ExpertGetFrame function</span></span>

<span data-ttu-id="952c7-104">**ExpertGetFrame** 函式會從載入的捕獲傳回要求的框架。</span><span class="sxs-lookup"><span data-stu-id="952c7-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="952c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="952c7-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="952c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="952c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="952c7-107">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952c7-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952c7-108">唯一的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="952c7-108">A unique expert identifier.</span></span> <span data-ttu-id="952c7-109">網路監視器在呼叫 [**Run**](run.md)函式時，將 *hExpertKey* 識別碼傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="952c7-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="952c7-110">*方向* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952c7-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952c7-111">識別網路監視器如何搜尋框架的值。</span><span class="sxs-lookup"><span data-stu-id="952c7-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="952c7-112">值</span><span class="sxs-lookup"><span data-stu-id="952c7-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="952c7-113">意義</span><span class="sxs-lookup"><span data-stu-id="952c7-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="952c7-114"><dt>**取得 \_ 指定的 \_ 框架**</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="952c7-115">傳回要求的框架。</span><span class="sxs-lookup"><span data-stu-id="952c7-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="952c7-116"><dt>**取得 \_ \_ 下一個畫面格 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="952c7-117">傳回下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="952c7-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="952c7-118"><dt>**取得 \_ \_ 下一個畫面格 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="952c7-119">傳回上一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="952c7-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="952c7-120">*RequestFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952c7-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952c7-121">旗標，指定網路監視器應該如何處理要求。</span><span class="sxs-lookup"><span data-stu-id="952c7-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="952c7-122">指定下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="952c7-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="952c7-123">值</span><span class="sxs-lookup"><span data-stu-id="952c7-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="952c7-124">意義</span><span class="sxs-lookup"><span data-stu-id="952c7-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="952c7-125"><dt>**旗標 \_ 延後 \_ 至 \_ UI \_ 篩選**</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="952c7-126">套用在 *hFilter* 中指定之專家的顯示篩選參數之前，請套用網路監視器在專家啟動時所使用的顯示篩選。</span><span class="sxs-lookup"><span data-stu-id="952c7-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="952c7-127"><dt>**旗標 \_ 附加 \_ 屬性**</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="952c7-128">所有通訊協定剖析器在此畫面格所宣告的區段中找到的屬性會附加至框架。</span><span class="sxs-lookup"><span data-stu-id="952c7-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="952c7-129">如果未設定旗標， **pEFrameDescriptor**) 所傳回之 [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md)結構 (的 **lpPropertyTable** 欄位將會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="952c7-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="952c7-130">*RequestedFrameNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952c7-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952c7-131">要求的框架數目。</span><span class="sxs-lookup"><span data-stu-id="952c7-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="952c7-132">*hFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952c7-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952c7-133">專家顯示篩選的控點。</span><span class="sxs-lookup"><span data-stu-id="952c7-133">A handle to the expert display filter.</span></span> <span data-ttu-id="952c7-134">如果專家沒有顯示篩選器，請將參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="952c7-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="952c7-135">*pEFrameDescriptor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="952c7-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="952c7-136">傳回的 [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) 結構，它會描述框架。</span><span class="sxs-lookup"><span data-stu-id="952c7-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="952c7-137">專家必須配置和釋放此結構所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="952c7-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="952c7-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="952c7-138">Return value</span></span>

<span data-ttu-id="952c7-139">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="952c7-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="952c7-140">如果函式不成功，則傳回值會指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="952c7-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="952c7-141">如果傳回值是 NMERR \_ 專家 \_ 終止，則專家必須立即清除並返回; 使用者已中止專家執行。</span><span class="sxs-lookup"><span data-stu-id="952c7-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="952c7-142">備註</span><span class="sxs-lookup"><span data-stu-id="952c7-142">Remarks</span></span>

<span data-ttu-id="952c7-143">如果您設定 FLAGS \_ 附加 \_ 屬性，呼叫所需的資源會比未設定旗標的資源還多。</span><span class="sxs-lookup"><span data-stu-id="952c7-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="952c7-144">如果未設定旗標，指標會指向原始框架和框架的相關資料。</span><span class="sxs-lookup"><span data-stu-id="952c7-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="952c7-145">如果設定此旗標，網路監視器會呼叫宣告框架一部分的每個剖析器，以將所有屬性附加至框架。</span><span class="sxs-lookup"><span data-stu-id="952c7-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="952c7-146">這可能是緩慢的進程。</span><span class="sxs-lookup"><span data-stu-id="952c7-146">This can be a slow process.</span></span>

<span data-ttu-id="952c7-147">\_ \_ 除非專家需要剖析器附加至框架的屬性，否則專家不應設定 FLAGS 附加屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="952c7-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="952c7-148">如果可能，專家應該在沒有旗標的情況下呼叫 **ExpertGetFrame** 函式，然後直接從框架中解壓縮所需的資料。</span><span class="sxs-lookup"><span data-stu-id="952c7-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="952c7-149">如果專家呼叫 **ExpertGetFrame** 時沒有旗標 \_ 附加 \_ 屬性旗標，且需要與該框架相關聯的屬性 (事件，例如) ，專家會使用相同的參數來呼叫 **ExpertGetFrame** ，但下列專案除外：</span><span class="sxs-lookup"><span data-stu-id="952c7-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="952c7-150">使用上述程式碼可確保專家取得所需的框架，而不需要再次呼叫篩選器程式碼。</span><span class="sxs-lookup"><span data-stu-id="952c7-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="952c7-151">您可以將 *hFilter* 參數設定為 **LPVOID**。</span><span class="sxs-lookup"><span data-stu-id="952c7-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="952c7-152">如果存在，則傳回的框架會傳遞此篩選器。</span><span class="sxs-lookup"><span data-stu-id="952c7-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="952c7-153">如果專家沒有可傳遞至函式的顯示篩選 (如果 *hFilter* 為 **Null** ) ，則不會篩選傳回的畫面格。</span><span class="sxs-lookup"><span data-stu-id="952c7-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="952c7-154">**ExpertGetFrame** 函式只能由執行 [**執行**](run.md)或 [**設定**](configure.md)匯出函數的專家呼叫。</span><span class="sxs-lookup"><span data-stu-id="952c7-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="952c7-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="952c7-155">Requirements</span></span>



| <span data-ttu-id="952c7-156">需求</span><span class="sxs-lookup"><span data-stu-id="952c7-156">Requirement</span></span> | <span data-ttu-id="952c7-157">值</span><span class="sxs-lookup"><span data-stu-id="952c7-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="952c7-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="952c7-158">Minimum supported client</span></span><br/> | <span data-ttu-id="952c7-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952c7-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="952c7-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="952c7-160">Minimum supported server</span></span><br/> | <span data-ttu-id="952c7-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952c7-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="952c7-162">標頭</span><span class="sxs-lookup"><span data-stu-id="952c7-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="952c7-163"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="952c7-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="952c7-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="952c7-165"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="952c7-166">DLL</span><span class="sxs-lookup"><span data-stu-id="952c7-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="952c7-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="952c7-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




