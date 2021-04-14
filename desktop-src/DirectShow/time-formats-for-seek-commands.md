---
description: 搜尋命令的時間格式
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: 搜尋命令的時間格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514212"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="e6522-103">搜尋命令的時間格式</span><span class="sxs-lookup"><span data-stu-id="e6522-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="e6522-104">**IMediaSeeking** 介面中的許多方法都具有表示位置值的參數，例如目前的位置或停止位置。</span><span class="sxs-lookup"><span data-stu-id="e6522-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="e6522-105">根據預設，這些參數會以100毫微秒的單位來表示，也稱為參考時間。</span><span class="sxs-lookup"><span data-stu-id="e6522-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="e6522-106">任何可以搜尋的篩選準則都必須支援依參考時間進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="e6522-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="e6522-107">某些篩選器也可以使用其他時間單位來搜尋，例如搜尋特定的框架編號，或搜尋資料流程內的指定位元組位移。</span><span class="sxs-lookup"><span data-stu-id="e6522-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="e6522-108">每個時間單位都稱為時間格式，而且是由全域唯一識別碼 (GUID) 所定義。</span><span class="sxs-lookup"><span data-stu-id="e6522-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="e6522-109">如需 DirectShow 所定義的時間格式清單，請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="e6522-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="e6522-110">協力廠商也可以定義自訂時間格式的 Guid。</span><span class="sxs-lookup"><span data-stu-id="e6522-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="e6522-111">若要判斷目前在篩選圖形中的篩選是否支援特定時間格式，請呼叫 [**IMediaSeeking：： IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) 方法。</span><span class="sxs-lookup"><span data-stu-id="e6522-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="e6522-112">如果支援格式，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e6522-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="e6522-113">否則，它會傳回 \_ FALSE 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e6522-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="e6522-114">如果支援格式，您可以藉由呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 方法切換為該格式。</span><span class="sxs-lookup"><span data-stu-id="e6522-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="e6522-115">如果 **SetTimeFormat** 方法成功，則會使用新的時間格式來表示後續的搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="e6522-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="e6522-116">下列範例會檢查圖形是否支援依框架編號搜尋。</span><span class="sxs-lookup"><span data-stu-id="e6522-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="e6522-117">如果是，則會搜尋框架編號20：</span><span class="sxs-lookup"><span data-stu-id="e6522-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="e6522-118">請注意，時間格式只適用于搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="e6522-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="e6522-119">它們不會影響圖形播放或其他動作。</span><span class="sxs-lookup"><span data-stu-id="e6522-119">They do not affect graph playback or other actions.</span></span>

 

 



