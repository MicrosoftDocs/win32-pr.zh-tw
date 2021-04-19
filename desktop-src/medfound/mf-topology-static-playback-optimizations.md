---
description: 啟用影片管線中的靜態優化。
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: 'MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975913"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="965c8-103">MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化屬性</span><span class="sxs-lookup"><span data-stu-id="965c8-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="965c8-104">啟用影片管線中的靜態優化。</span><span class="sxs-lookup"><span data-stu-id="965c8-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="965c8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="965c8-105">Data type</span></span>

<span data-ttu-id="965c8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="965c8-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="965c8-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="965c8-107">Get/set</span></span>

<span data-ttu-id="965c8-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="965c8-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="965c8-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="965c8-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="965c8-110">適用於</span><span class="sxs-lookup"><span data-stu-id="965c8-110">Applies to</span></span>

[<span data-ttu-id="965c8-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="965c8-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="965c8-112">備註</span><span class="sxs-lookup"><span data-stu-id="965c8-112">Remarks</span></span>

<span data-ttu-id="965c8-113">請先設定這個屬性，然後再載入拓撲。</span><span class="sxs-lookup"><span data-stu-id="965c8-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="965c8-114">如果屬性為 **TRUE**，拓撲載入器會嘗試在播放開始之前將管線優化。</span><span class="sxs-lookup"><span data-stu-id="965c8-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="965c8-115">如果設定此屬性，您也應該設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="965c8-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="965c8-116">MF \_ 拓撲 \_ 播放 \_ 畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="965c8-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="965c8-117">MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="965c8-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="965c8-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="965c8-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="965c8-119">範例</span><span class="sxs-lookup"><span data-stu-id="965c8-119">Examples</span></span>


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="965c8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="965c8-120">Requirements</span></span>



| <span data-ttu-id="965c8-121">需求</span><span class="sxs-lookup"><span data-stu-id="965c8-121">Requirement</span></span> | <span data-ttu-id="965c8-122">值</span><span class="sxs-lookup"><span data-stu-id="965c8-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="965c8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="965c8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="965c8-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="965c8-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="965c8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="965c8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="965c8-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="965c8-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="965c8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="965c8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="965c8-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="965c8-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965c8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="965c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965c8-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="965c8-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="965c8-131">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="965c8-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="965c8-132">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="965c8-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




