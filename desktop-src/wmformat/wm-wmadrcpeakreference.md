---
title: WM/WMADRCPeakReference
description: WM/WMADRCPeakReference 屬性包含檔案的最大磁片區層級（編碼方式）。 動態範圍控制的 Windows Media Player 會使用這個值。 此值是由編解碼器設定的，而且是唯讀的。
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- WM/WMADRCPeakReference windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373148"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="beeb4-106">WM/WMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="beeb4-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="beeb4-107">**WM/WMADRCPeakReference** 屬性包含檔案的最大磁片區層級（編碼方式）。</span><span class="sxs-lookup"><span data-stu-id="beeb4-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="beeb4-108">動態範圍控制的 Windows Media Player 會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="beeb4-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="beeb4-109">此值是由編解碼器設定的，而且是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="beeb4-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="beeb4-110">全域常數</span><span class="sxs-lookup"><span data-stu-id="beeb4-110">Global Constant</span></span>

<span data-ttu-id="beeb4-111">g \_ wszWMWMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="beeb4-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="beeb4-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="beeb4-112">Data Type</span></span>

<span data-ttu-id="beeb4-113">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="beeb4-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="beeb4-114">備註</span><span class="sxs-lookup"><span data-stu-id="beeb4-114">Remarks</span></span>

<span data-ttu-id="beeb4-115">有四個屬性用於動態範圍控制的 Windows Media Player： **wm/WMADRCAverageReference**、 **wm/WMADRCPeakReference**、 **wm/WMADRCAverageTarget** 和 **WM/WMADRCPeakTarget**。</span><span class="sxs-lookup"><span data-stu-id="beeb4-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="beeb4-116">使用 Windows Media 音訊9編解碼器或 Windows Media 音訊 9 Professional 編解碼器撰寫串流時，寫入器會根據編解碼器的資訊來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="beeb4-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="beeb4-117">平均值會設定為數據流的平均磁片區層級，而尖峰值會設定為數據流中的最大磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="beeb4-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="beeb4-118">參考值是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="beeb4-118">The reference values are read-only.</span></span> <span data-ttu-id="beeb4-119">當播放檔案以記錄使用者的動態範圍控制喜好設定時，會 Windows Media Player 設定目標值。</span><span class="sxs-lookup"><span data-stu-id="beeb4-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="beeb4-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="beeb4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beeb4-121">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="beeb4-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="beeb4-122">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="beeb4-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="beeb4-123">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="beeb4-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="beeb4-124">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="beeb4-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




