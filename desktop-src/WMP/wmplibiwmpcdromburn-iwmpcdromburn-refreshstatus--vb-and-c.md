---
title: IWMPCdromBurn refreshStatus 方法
description: RefreshStatus 方法會更新目前燒錄播放清單的狀態資訊。
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- refreshStatus 方法 Windows Media Player
- refreshStatus 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，refreshStatus 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993405"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="86bea-106">IWMPCdromBurn：： refreshStatus 方法</span><span class="sxs-lookup"><span data-stu-id="86bea-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="86bea-107">**RefreshStatus** 方法會更新目前燒錄播放清單的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="86bea-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="86bea-108">語法</span><span class="sxs-lookup"><span data-stu-id="86bea-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="86bea-109">參數</span><span class="sxs-lookup"><span data-stu-id="86bea-109">Parameters</span></span>

<span data-ttu-id="86bea-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="86bea-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86bea-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="86bea-111">Return value</span></span>

<span data-ttu-id="86bea-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="86bea-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86bea-113">備註</span><span class="sxs-lookup"><span data-stu-id="86bea-113">Remarks</span></span>

<span data-ttu-id="86bea-114">在您建立或變更燒錄播放清單之後，請先呼叫這個方法，然後再閱讀狀態資訊或燒錄 CD。</span><span class="sxs-lookup"><span data-stu-id="86bea-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="86bea-115">您可以藉由取得 **burnState** 和檢查 wmpbsRefreshStatusPending 的值，測試是否需要重新整理。</span><span class="sxs-lookup"><span data-stu-id="86bea-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="86bea-116">重新整理狀態是一項同步作業。</span><span class="sxs-lookup"><span data-stu-id="86bea-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="86bea-117">這表示，如果目前的燒錄播放清單是大型的，而且包含許多變更，則此方法會傳回較長的一段時間。</span><span class="sxs-lookup"><span data-stu-id="86bea-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="86bea-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="86bea-118">Requirements</span></span>



| <span data-ttu-id="86bea-119">需求</span><span class="sxs-lookup"><span data-stu-id="86bea-119">Requirement</span></span> | <span data-ttu-id="86bea-120">值</span><span class="sxs-lookup"><span data-stu-id="86bea-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86bea-121">版本</span><span class="sxs-lookup"><span data-stu-id="86bea-121">Version</span></span><br/>   | <span data-ttu-id="86bea-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="86bea-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="86bea-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="86bea-123">Namespace</span></span><br/> | <span data-ttu-id="86bea-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="86bea-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="86bea-125">組件</span><span class="sxs-lookup"><span data-stu-id="86bea-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="86bea-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="86bea-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86bea-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86bea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86bea-128">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="86bea-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="86bea-129">**IWMPCdromBurn. burnState (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="86bea-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="86bea-130">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="86bea-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





