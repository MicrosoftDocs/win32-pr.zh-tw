---
description: <span id="vspixengine.callbackcommandtype"></span>CallbackCommandType 列舉-用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallbackCommandType 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090126"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="2973f-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType 列舉</span><span class="sxs-lookup"><span data-stu-id="2973f-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="2973f-104">用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。</span><span class="sxs-lookup"><span data-stu-id="2973f-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="2973f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2973f-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="2973f-106">常數</span><span class="sxs-lookup"><span data-stu-id="2973f-106">Constants</span></span>

<span data-ttu-id="2973f-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="2973f-108">來自 BeginCommunication 的結果。</span><span class="sxs-lookup"><span data-stu-id="2973f-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="2973f-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="2973f-110">錯誤。</span><span class="sxs-lookup"><span data-stu-id="2973f-110">Errors.</span></span>

<span data-ttu-id="2973f-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="2973f-112">警告：</span><span class="sxs-lookup"><span data-stu-id="2973f-112">Warnings.</span></span>

<span data-ttu-id="2973f-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="2973f-114">訊息。</span><span class="sxs-lookup"><span data-stu-id="2973f-114">Messages.</span></span>

<span data-ttu-id="2973f-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="2973f-116">來自 RunExperiment 的結果。</span><span class="sxs-lookup"><span data-stu-id="2973f-116">Result from RunExperiment.</span></span>

<span data-ttu-id="2973f-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="2973f-118">來自 RunAction 的結果。</span><span class="sxs-lookup"><span data-stu-id="2973f-118">Result from RunAction.</span></span>

<span data-ttu-id="2973f-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="2973f-120">值，這個值表示當已捕捉新框架並可供顯示時，所要呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="2973f-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="2973f-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span><span class="sxs-lookup"><span data-stu-id="2973f-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="2973f-122">在 Windows 7 和 Windows 8 上使用的舊版 BeginCommunication 結果。</span><span class="sxs-lookup"><span data-stu-id="2973f-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="2973f-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="2973f-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="2973f-124">來自 RunExperiementProgress 的結果。</span><span class="sxs-lookup"><span data-stu-id="2973f-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="2973f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2973f-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2973f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2973f-126">Header</span></span></p></td><td><span data-ttu-id="2973f-127">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="2973f-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



