---
description: 開始對著色器進行調試的要求。 此要求包含兩個部分：產生追蹤，以及對追蹤進行 debug 錯。
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109249"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="c8283-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 介面</span><span class="sxs-lookup"><span data-stu-id="c8283-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="c8283-105">開始對著色器進行調試的要求。</span><span class="sxs-lookup"><span data-stu-id="c8283-105">Request to start debugging a shader.</span></span> <span data-ttu-id="c8283-106">此要求包含兩個部分：產生追蹤，以及對追蹤進行 debug 錯。</span><span class="sxs-lookup"><span data-stu-id="c8283-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="c8283-107">成員</span><span class="sxs-lookup"><span data-stu-id="c8283-107">Members</span></span>

<span data-ttu-id="c8283-108">**IDebugShaderRequest2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c8283-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c8283-109">**IDebugShaderRequest2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c8283-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="c8283-110">方法</span><span class="sxs-lookup"><span data-stu-id="c8283-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c8283-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="c8283-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c8283-112">**IDebugShaderRequest2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c8283-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c8283-113">方法</span><span class="sxs-lookup"><span data-stu-id="c8283-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c8283-114">描述</span><span class="sxs-lookup"><span data-stu-id="c8283-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c8283-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8283-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8283-116">要求開始對指定的資訊清單進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c8283-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c8283-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8283-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8283-118">在 debug 要求中產生著色器追蹤指令的要求。</span><span class="sxs-lookup"><span data-stu-id="c8283-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="c8283-119">以追蹤為基礎的偵錯工具會發生在 CPU (變形) ，而不是 GPU。</span><span class="sxs-lookup"><span data-stu-id="c8283-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c8283-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8283-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c8283-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c8283-121">Header</span></span></p></td><td><span data-ttu-id="c8283-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="c8283-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
