---
title: WM/WMADRCPeakTarget
description: WM/WMADRCPeakTarget 屬性包含使用者要求的最大磁片區層級。 動態範圍控制的 Windows Media Player 會使用這個值。
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- WM/WMADRCPeakTarget windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678607"
---
# <a name="wmwmadrcpeaktarget"></a><span data-ttu-id="0d8d0-105">WM/WMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="0d8d0-105">WM/WMADRCPeakTarget</span></span>

<span data-ttu-id="0d8d0-106">**WM/WMADRCPeakTarget** 屬性包含使用者要求的最大磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-106">The **WM/WMADRCPeakTarget** attribute contains the maximum volume level requested by the user.</span></span> <span data-ttu-id="0d8d0-107">動態範圍控制的 Windows Media Player 會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0d8d0-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="0d8d0-108">Global Constant</span></span>

<span data-ttu-id="0d8d0-109">g \_ wszWMWMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="0d8d0-109">g\_wszWMWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="0d8d0-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="0d8d0-110">Data Type</span></span>

<span data-ttu-id="0d8d0-111">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0d8d0-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8d0-112">備註</span><span class="sxs-lookup"><span data-stu-id="0d8d0-112">Remarks</span></span>

<span data-ttu-id="0d8d0-113">有四個屬性用於動態範圍控制的 Windows Media Player： **wm/WMADRCAverageReference**、 **wm/WMADRCPeakReference**、 **wm/WMADRCAverageTarget** 和 **WM/WMADRCPeakTarget**。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="0d8d0-114">使用 Windows Media 音訊9編解碼器或 Windows Media 音訊 9 Professional 編解碼器撰寫串流時，寫入器會根據編解碼器的資訊來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="0d8d0-115">平均值會設定為數據流的平均磁片區層級，而尖峰值會設定為數據流中的最大磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="0d8d0-116">參考值是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-116">The reference values are read-only.</span></span> <span data-ttu-id="0d8d0-117">當播放檔案以記錄使用者的動態範圍控制喜好設定時，會 Windows Media Player 設定目標值。</span><span class="sxs-lookup"><span data-stu-id="0d8d0-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d8d0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d8d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8d0-119">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="0d8d0-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="0d8d0-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="0d8d0-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="0d8d0-121">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="0d8d0-121">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="0d8d0-122">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="0d8d0-122">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




