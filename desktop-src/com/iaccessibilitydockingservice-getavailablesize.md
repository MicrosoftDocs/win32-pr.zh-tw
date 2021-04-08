---
title: IAccessibilityDockingService GetAvailableSize 方法
description: 取得可在監視器上停駐協助工具視窗的可用維度。
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- GetAvailableSize 方法 COM
- GetAvailableSize 方法 COM，IAccessibilityDockingService 介面
- IAccessibilityDockingService 介面 COM，GetAvailableSize 方法
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022416"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="73863-106">IAccessibilityDockingService：： GetAvailableSize 方法</span><span class="sxs-lookup"><span data-stu-id="73863-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="73863-107">取得可在監視器上停駐協助工具視窗的可用維度。</span><span class="sxs-lookup"><span data-stu-id="73863-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="73863-108">語法</span><span class="sxs-lookup"><span data-stu-id="73863-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="73863-109">參數</span><span class="sxs-lookup"><span data-stu-id="73863-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73863-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73863-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73863-111">指定將抓取可用停駐大小的監視器。</span><span class="sxs-lookup"><span data-stu-id="73863-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="73863-112">*puMaxHeight* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="73863-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73863-113">成功時，請將設定為指定 *hMonitor* 上可停駐的最大高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="73863-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="73863-114">失敗時，請設定為零。</span><span class="sxs-lookup"><span data-stu-id="73863-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="73863-115">*puFixedWidth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="73863-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73863-116">成功時，請將設定為固定寬度（可在指定的 *hMonitor* 上銜接）（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="73863-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="73863-117">停駐至此 *hMonitor* 的任何視窗將會調整為此寬度。</span><span class="sxs-lookup"><span data-stu-id="73863-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="73863-118">失敗時，請設定為零。</span><span class="sxs-lookup"><span data-stu-id="73863-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73863-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="73863-119">Return value</span></span>



| <span data-ttu-id="73863-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="73863-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="73863-121">Description</span><span class="sxs-lookup"><span data-stu-id="73863-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73863-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="73863-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="73863-123">成功。</span><span class="sxs-lookup"><span data-stu-id="73863-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="73863-124"><dt>**\_WIN32 中的 HRESULT \_ (錯誤 \_ 不正確 \_ 監視器 \_ 控制碼)**</dt></span><span class="sxs-lookup"><span data-stu-id="73863-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="73863-125">監視器控制碼所指定的監視器不支援停駐。</span><span class="sxs-lookup"><span data-stu-id="73863-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="73863-126">如果 *puMaxHeight* 或 *puFixedWidth* 為 null，則會發生存取違規。</span><span class="sxs-lookup"><span data-stu-id="73863-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="73863-127">備註</span><span class="sxs-lookup"><span data-stu-id="73863-127">Remarks</span></span>

<span data-ttu-id="73863-128">協助工具視窗只能停駐在至少具有768垂直螢幕圖元的監視器上。</span><span class="sxs-lookup"><span data-stu-id="73863-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="73863-129">此 API 不會允許這類視窗銜接高度，而導致 Windows Store 應用程式的垂直螢幕圖元小於768。</span><span class="sxs-lookup"><span data-stu-id="73863-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="73863-130">範例</span><span class="sxs-lookup"><span data-stu-id="73863-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="73863-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73863-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73863-132">**IAccessibilityDockingService**</span><span class="sxs-lookup"><span data-stu-id="73863-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





