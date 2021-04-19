---
description: 用來將回應從捕捉引擎傳送至圖形診斷的列舉。
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixPipeResponse 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986229"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="e4984-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse 列舉</span><span class="sxs-lookup"><span data-stu-id="e4984-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="e4984-104">用來將回應從捕捉引擎傳送至圖形診斷的列舉。</span><span class="sxs-lookup"><span data-stu-id="e4984-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4984-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4984-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="e4984-106">常數</span><span class="sxs-lookup"><span data-stu-id="e4984-106">Constants</span></span>

<span data-ttu-id="e4984-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**可用的新 \_ 資料 \_**</span><span class="sxs-lookup"><span data-stu-id="e4984-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="e4984-108">指出新資料已寫入圖形記錄檔並可供讀取的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="e4984-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**實驗 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="e4984-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="e4984-110">指出有關 capture 會話設定資訊的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="e4984-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**錯誤碼**</span><span class="sxs-lookup"><span data-stu-id="e4984-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="e4984-112">表示捕獲引擎發生錯誤的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="e4984-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="e4984-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="e4984-114">表示 capture 引擎已開始捕獲圖形資訊的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="e4984-115">這並不表示資料仍可供檢查。</span><span class="sxs-lookup"><span data-stu-id="e4984-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="e4984-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**部分 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="e4984-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="e4984-117">指出部分資料已寫入圖形記錄檔的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="e4984-118"><span id="READY"></span><span id="ready"></span>**準備**</span><span class="sxs-lookup"><span data-stu-id="e4984-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="e4984-119">表示 capture 引擎已準備好開始捕獲圖形資訊的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="e4984-120"><span id="DONE"></span><span id="done"></span>**做**</span><span class="sxs-lookup"><span data-stu-id="e4984-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="e4984-121">內部</span><span class="sxs-lookup"><span data-stu-id="e4984-121">Internal</span></span>

<span data-ttu-id="e4984-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span><span class="sxs-lookup"><span data-stu-id="e4984-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="e4984-123">表示已啟動框架捕獲的回應。</span><span class="sxs-lookup"><span data-stu-id="e4984-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="e4984-124"><span id="STATUS"></span><span id="status"></span>**地位**</span><span class="sxs-lookup"><span data-stu-id="e4984-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="e4984-125">指出所要捕捉之應用程式狀態資訊的回應;例如，以畫面播放速率表示。</span><span class="sxs-lookup"><span data-stu-id="e4984-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4984-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4984-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e4984-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e4984-127">Header</span></span></p></td><td><span data-ttu-id="e4984-128">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e4984-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



