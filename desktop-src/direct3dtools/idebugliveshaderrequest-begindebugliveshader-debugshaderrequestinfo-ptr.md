---
description: 在 GPU 上偵測著色器的要求 (即時調試) vs CPU (以追蹤為基礎的調試) 。
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugLiveShaderRequest：： BeginDebugLiveShader 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688052"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span data-ttu-id="219ae-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest：： BeginDebugLiveShader 方法</span><span class="sxs-lookup"><span data-stu-id="219ae-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest::BeginDebugLiveShader method</span></span>

<span data-ttu-id="219ae-104">在 GPU 上偵測著色器的要求 (即時調試) vs CPU (以追蹤為基礎的調試) 。</span><span class="sxs-lookup"><span data-stu-id="219ae-104">Requests to debug a shader on the GPU (live debugging) vs CPU (trace-based debugging).</span></span>

## <a name="syntax"></a><span data-ttu-id="219ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="219ae-105">Syntax</span></span>


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a><span data-ttu-id="219ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="219ae-106">Parameters</span></span>

<span data-ttu-id="219ae-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="219ae-107">*requestInfo* </span></span>  
<span data-ttu-id="219ae-108">描述要求的事件/頂點/圖元之 DebugShaderRequestInfo 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="219ae-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

## <a name="return-value"></a><span data-ttu-id="219ae-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="219ae-109">Return value</span></span>

<span data-ttu-id="219ae-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="219ae-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="219ae-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="219ae-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="219ae-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="219ae-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="219ae-113">標頭</span><span class="sxs-lookup"><span data-stu-id="219ae-113">Header</span></span></p></td><td><span data-ttu-id="219ae-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="219ae-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="219ae-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="219ae-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="219ae-116">**IDebugLiveShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="219ae-116">**IDebugLiveShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
