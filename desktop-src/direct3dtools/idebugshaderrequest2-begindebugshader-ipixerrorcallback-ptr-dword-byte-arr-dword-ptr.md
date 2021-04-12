---
description: 要求開始對指定的資訊清單進行偵錯工具。
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2：： BeginDebugShader 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109253"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="c6777-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2：： BeginDebugShader 方法</span><span class="sxs-lookup"><span data-stu-id="c6777-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="c6777-104">要求開始對指定的資訊清單進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c6777-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6777-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6777-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="c6777-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6777-106">Parameters</span></span>

<span data-ttu-id="c6777-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="c6777-107">*errorCallback* </span></span>  
<span data-ttu-id="c6777-108">偵錯工具期間可能發生的錯誤回呼位址。</span><span class="sxs-lookup"><span data-stu-id="c6777-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="c6777-109">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="c6777-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="c6777-110">指令資料流程中的指令數目。</span><span class="sxs-lookup"><span data-stu-id="c6777-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="c6777-111">*count1 \_ instructionStream* </span><span class="sxs-lookup"><span data-stu-id="c6777-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="c6777-112">指定的指令資料流程。</span><span class="sxs-lookup"><span data-stu-id="c6777-112">The specified instruction stream.</span></span>

<span data-ttu-id="c6777-113">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="c6777-113">*pDevice* </span></span>  
<span data-ttu-id="c6777-114">要傳遞至偵測引擎以便與此 (的偵測引擎進行通訊的位址) 的 readprocessmemory debug engine。</span><span class="sxs-lookup"><span data-stu-id="c6777-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="c6777-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6777-115">Return value</span></span>

<span data-ttu-id="c6777-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c6777-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6777-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6777-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6777-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6777-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c6777-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c6777-119">Header</span></span></p></td><td><span data-ttu-id="c6777-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="c6777-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c6777-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6777-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c6777-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="c6777-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
