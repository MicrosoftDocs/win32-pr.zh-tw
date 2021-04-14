---
description: 裝置傳輸狀態
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: 裝置傳輸狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385842"
---
# <a name="device-transport-state"></a><span data-ttu-id="12b69-103">裝置傳輸狀態</span><span class="sxs-lookup"><span data-stu-id="12b69-103">Device Transport State</span></span>

<span data-ttu-id="12b69-104">若要取得裝置的目前狀態（例如播放、暫停或停止），請呼叫 [**IAMExtTransport：： get \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) 方法。</span><span class="sxs-lookup"><span data-stu-id="12b69-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="12b69-105">方法會抓取指出裝置狀態的常數：</span><span class="sxs-lookup"><span data-stu-id="12b69-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="12b69-106">值</span><span class="sxs-lookup"><span data-stu-id="12b69-106">Value</span></span>                    | <span data-ttu-id="12b69-107">裝置狀態</span><span class="sxs-lookup"><span data-stu-id="12b69-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="12b69-108">ED \_ 模式 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="12b69-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="12b69-109">播放</span><span class="sxs-lookup"><span data-stu-id="12b69-109">Play</span></span>         |
| <span data-ttu-id="12b69-110">ED \_ 模式 \_ 停止</span><span class="sxs-lookup"><span data-stu-id="12b69-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="12b69-111">停止</span><span class="sxs-lookup"><span data-stu-id="12b69-111">Stop</span></span>         |
| <span data-ttu-id="12b69-112">ED \_ 模式 \_ 凍結</span><span class="sxs-lookup"><span data-stu-id="12b69-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="12b69-113">暫停</span><span class="sxs-lookup"><span data-stu-id="12b69-113">Pause</span></span>        |
| <span data-ttu-id="12b69-114">ED \_ 模式 \_ FF</span><span class="sxs-lookup"><span data-stu-id="12b69-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="12b69-115">向前快轉</span><span class="sxs-lookup"><span data-stu-id="12b69-115">Fast-forward</span></span> |
| <span data-ttu-id="12b69-116">ED \_ 模式 \_ 倒轉</span><span class="sxs-lookup"><span data-stu-id="12b69-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="12b69-117">Rewind</span><span class="sxs-lookup"><span data-stu-id="12b69-117">Rewind</span></span>       |
| <span data-ttu-id="12b69-118">ED \_ 模式 \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="12b69-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="12b69-119">Record</span><span class="sxs-lookup"><span data-stu-id="12b69-119">Record</span></span>       |
| <span data-ttu-id="12b69-120">ED \_ 模式 \_ 記錄 \_ 凍結</span><span class="sxs-lookup"><span data-stu-id="12b69-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="12b69-121">記錄-暫停</span><span class="sxs-lookup"><span data-stu-id="12b69-121">Record-pause</span></span> |



 

<span data-ttu-id="12b69-122">下列程式碼會檢查裝置狀態：</span><span class="sxs-lookup"><span data-stu-id="12b69-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="12b69-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="12b69-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b69-124">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="12b69-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



