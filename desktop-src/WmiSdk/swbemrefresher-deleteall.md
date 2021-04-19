---
description: SWbemRefresher. DeleteAll 方法會從 SWbemRefresher 物件中的集合中移除所有專案。SWbemRefresher 物件。
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: 'SWbemRefresher. DeleteAll 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982802"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="17a10-103">SWbemRefresher. DeleteAll 方法</span><span class="sxs-lookup"><span data-stu-id="17a10-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="17a10-104">**SWbemRefresher. DeleteAll** 方法會從 [**SWbemRefresher**](swbemrefresher.md)物件中的集合中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="17a10-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="17a10-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="17a10-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17a10-106">語法</span><span class="sxs-lookup"><span data-stu-id="17a10-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="17a10-107">參數</span><span class="sxs-lookup"><span data-stu-id="17a10-107">Parameters</span></span>

<span data-ttu-id="17a10-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="17a10-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17a10-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="17a10-109">Return value</span></span>

<span data-ttu-id="17a10-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="17a10-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a10-111">備註</span><span class="sxs-lookup"><span data-stu-id="17a10-111">Remarks</span></span>

<span data-ttu-id="17a10-112">每個已移除專案的對應 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 都會將其 [**複習**](swbemrefreshableitem-refresher.md) 屬性設為 **Null**，這表示它不再有父重新整理程式。</span><span class="sxs-lookup"><span data-stu-id="17a10-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a10-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a10-113">Requirements</span></span>



| <span data-ttu-id="17a10-114">需求</span><span class="sxs-lookup"><span data-stu-id="17a10-114">Requirement</span></span> | <span data-ttu-id="17a10-115">值</span><span class="sxs-lookup"><span data-stu-id="17a10-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a10-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17a10-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17a10-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17a10-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17a10-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17a10-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17a10-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17a10-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17a10-120">標頭</span><span class="sxs-lookup"><span data-stu-id="17a10-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a10-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="17a10-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17a10-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17a10-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="17a10-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17a10-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17a10-124">DLL</span><span class="sxs-lookup"><span data-stu-id="17a10-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a10-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a10-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="17a10-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="17a10-126">CLSID</span></span><br/>                    | <span data-ttu-id="17a10-127">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="17a10-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="17a10-128">IID</span><span class="sxs-lookup"><span data-stu-id="17a10-128">IID</span></span><br/>                      | <span data-ttu-id="17a10-129">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="17a10-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="17a10-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17a10-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a10-131">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="17a10-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




