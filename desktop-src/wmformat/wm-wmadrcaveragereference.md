---
title: WM/WMADRCAverageReference
description: WM/WMADRCAverageReference 屬性包含檔案的平均磁片區層級（編碼方式）。
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- WM/WMADRCAverageReference windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967231"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="43eb6-104">WM/WMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="43eb6-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="43eb6-105">**WM/WMADRCAverageReference** 屬性包含檔案的平均磁片區層級（編碼方式）。</span><span class="sxs-lookup"><span data-stu-id="43eb6-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="43eb6-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="43eb6-106">Global Constant</span></span>

<span data-ttu-id="43eb6-107">g \_ wszWMWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="43eb6-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="43eb6-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="43eb6-108">Data Type</span></span>

<span data-ttu-id="43eb6-109">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="43eb6-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="43eb6-110">備註</span><span class="sxs-lookup"><span data-stu-id="43eb6-110">Remarks</span></span>

<span data-ttu-id="43eb6-111">有四個屬性用於動態範圍控制的 Windows Media Player： **wm/WMADRCAverageReference**、 **wm/WMADRCPeakReference**、 **wm/WMADRCAverageTarget** 和 **WM/WMADRCPeakTarget**。</span><span class="sxs-lookup"><span data-stu-id="43eb6-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="43eb6-112">使用 Windows Media 音訊9編解碼器或 Windows Media 音訊 9 Professional 編解碼器撰寫串流時，寫入器會根據編解碼器的資訊來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="43eb6-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="43eb6-113">平均值會設定為數據流的平均磁片區層級，而尖峰值會設定為數據流中的最大磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="43eb6-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="43eb6-114">參考值是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="43eb6-114">The reference values are read-only.</span></span> <span data-ttu-id="43eb6-115">當播放檔案以記錄使用者的動態範圍控制喜好設定時，會 Windows Media Player 設定目標值。</span><span class="sxs-lookup"><span data-stu-id="43eb6-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="43eb6-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43eb6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43eb6-117">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="43eb6-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="43eb6-118">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="43eb6-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="43eb6-119">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="43eb6-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="43eb6-120">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="43eb6-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




