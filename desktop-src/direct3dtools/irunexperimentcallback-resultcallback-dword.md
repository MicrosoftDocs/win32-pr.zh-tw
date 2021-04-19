---
description: 在指定的進程上執行實驗 (capture) 的要求。
MS-HAID: vspixengine.IRunExperimentCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IRunExperimentCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C00034DF-5F51-49A2-B49A-62F98EA48F46
api_name:
- IRunExperimentCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ac6838e7103970d588814bdc5a39e9e26fd4a33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970878"
---
# <a name="span-idvspixengineirunexperimentcallback_resultcallback_dwordspanirunexperimentcallbackresultcallback-method"></a><span data-ttu-id="3d4b7-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>IRunExperimentCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="3d4b7-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>IRunExperimentCallback::ResultCallback method</span></span>

<span data-ttu-id="3d4b7-104">在指定的進程上執行實驗 (capture) 的要求。</span><span class="sxs-lookup"><span data-stu-id="3d4b7-104">Requests to run an experiment (capture) on the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d4b7-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD processId
);
```

## <a name="parameters"></a><span data-ttu-id="3d4b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d4b7-106">Parameters</span></span>

<span data-ttu-id="3d4b7-107">*進程* </span><span class="sxs-lookup"><span data-stu-id="3d4b7-107">*processId* </span></span>  
<span data-ttu-id="3d4b7-108">指定的進程。</span><span class="sxs-lookup"><span data-stu-id="3d4b7-108">The specified process.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d4b7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d4b7-109">Return value</span></span>

<span data-ttu-id="3d4b7-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3d4b7-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d4b7-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3d4b7-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4b7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d4b7-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3d4b7-113">標頭</span><span class="sxs-lookup"><span data-stu-id="3d4b7-113">Header</span></span></p></td><td><span data-ttu-id="3d4b7-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="3d4b7-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3d4b7-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d4b7-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3d4b7-116">**IRunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="3d4b7-116">**IRunExperimentCallback**</span></span>](/windows/desktop/direct3dtools/irunexperimentcallback)

 

 
