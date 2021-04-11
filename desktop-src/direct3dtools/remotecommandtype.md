---
description: 用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RemoteCommandType 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63b94ace0818e2057a87c0f3962bb3967843bcfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025768"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="de706-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType 列舉</span><span class="sxs-lookup"><span data-stu-id="de706-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="de706-104">用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。</span><span class="sxs-lookup"><span data-stu-id="de706-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="de706-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de706-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="de706-106">常數</span><span class="sxs-lookup"><span data-stu-id="de706-106">Constants</span></span>

<span data-ttu-id="de706-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span><span class="sxs-lookup"><span data-stu-id="de706-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="de706-108">開始通訊。</span><span class="sxs-lookup"><span data-stu-id="de706-108">Starts communication.</span></span>

<span data-ttu-id="de706-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span><span class="sxs-lookup"><span data-stu-id="de706-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="de706-110"> (實驗) 啟動圖形診斷 capture 會話。</span><span class="sxs-lookup"><span data-stu-id="de706-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="de706-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span><span class="sxs-lookup"><span data-stu-id="de706-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="de706-112">啟動抓取 (與按下列印畫面) 相同。</span><span class="sxs-lookup"><span data-stu-id="de706-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="de706-113">在捕獲框架時由主機傳送。</span><span class="sxs-lookup"><span data-stu-id="de706-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="de706-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="de706-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="de706-115">標頭</span><span class="sxs-lookup"><span data-stu-id="de706-115">Header</span></span></p></td><td><span data-ttu-id="de706-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="de706-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



