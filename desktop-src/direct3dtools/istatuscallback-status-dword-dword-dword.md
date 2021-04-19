---
description: 用來通知主機引擎進度的回呼函數。 這也可做為主機判斷引擎是否仍在執行中的方式。
title: IStatusCallback：： Status 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972321"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="fd5ee-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback：： Status 方法</span><span class="sxs-lookup"><span data-stu-id="fd5ee-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="fd5ee-105">用來通知主機引擎進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="fd5ee-106">這也可做為主機判斷引擎是否仍在執行中的方式。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5ee-107">語法</span><span class="sxs-lookup"><span data-stu-id="fd5ee-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="fd5ee-108">參數</span><span class="sxs-lookup"><span data-stu-id="fd5ee-108">Parameters</span></span>

<span data-ttu-id="fd5ee-109">*dwMillisecondsElapsed* </span><span class="sxs-lookup"><span data-stu-id="fd5ee-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="fd5ee-110">自上次撥號狀態以來經過的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="fd5ee-111">*dwFramesCaptured* </span><span class="sxs-lookup"><span data-stu-id="fd5ee-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="fd5ee-112">自上次撥號狀態以來已捕捉的框架數目。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="fd5ee-113">*dwFramesElapsed* </span><span class="sxs-lookup"><span data-stu-id="fd5ee-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="fd5ee-114">自上次撥號狀態以來經過的框架數目。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd5ee-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd5ee-115">Return value</span></span>

<span data-ttu-id="fd5ee-116">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="fd5ee-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fd5ee-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5ee-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd5ee-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fd5ee-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fd5ee-119">Header</span></span></p></td><td><span data-ttu-id="fd5ee-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fd5ee-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fd5ee-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd5ee-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fd5ee-122">**IStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="fd5ee-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
