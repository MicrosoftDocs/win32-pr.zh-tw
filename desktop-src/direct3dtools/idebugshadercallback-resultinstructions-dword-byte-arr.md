---
description: 回呼，會通知主機相關要求所傳回的 instructrion 資訊。
MS-HAID: vspixengine.IDebugShaderCallback\_ResultInstructions\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderCallback：： ResultInstructions 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 52440CE4-561C-4808-BE6A-B25A84BA5729
api_name:
- IDebugShaderCallback.ResultInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63dfd0e3b2b4ec7bd765e5fc0c85835f2a3ce102
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467749"
---
# <a name="span-idvspixengineidebugshadercallback_resultinstructions_dword_byte_arrspanidebugshadercallbackresultinstructions-method"></a><span data-ttu-id="d8391-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback：： ResultInstructions 方法</span><span class="sxs-lookup"><span data-stu-id="d8391-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback::ResultInstructions method</span></span>

<span data-ttu-id="d8391-104">回呼，會通知主機相關要求所傳回的 instructrion 資訊。</span><span class="sxs-lookup"><span data-stu-id="d8391-104">A callback that notifies the host of instructrion information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8391-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8391-105">Syntax</span></span>


```C++
HRESULT ResultInstructions(
   DWORD   instructionStreamSize,
   BYTE [] count0_instructionStream
);
```

## <a name="parameters"></a><span data-ttu-id="d8391-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8391-106">Parameters</span></span>

<span data-ttu-id="d8391-107">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="d8391-107">*instructionStreamSize* </span></span>  
<span data-ttu-id="d8391-108">指示的數目。</span><span class="sxs-lookup"><span data-stu-id="d8391-108">The number of instructions.</span></span>

<span data-ttu-id="d8391-109">*count0 \_ instructionStream* </span><span class="sxs-lookup"><span data-stu-id="d8391-109">*count0\_instructionStream* </span></span>  
<span data-ttu-id="d8391-110">指示。</span><span class="sxs-lookup"><span data-stu-id="d8391-110">The instructions.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8391-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8391-111">Return value</span></span>

<span data-ttu-id="d8391-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d8391-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8391-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d8391-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8391-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8391-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d8391-115">標頭</span><span class="sxs-lookup"><span data-stu-id="d8391-115">Header</span></span></p></td><td><span data-ttu-id="d8391-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="d8391-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d8391-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8391-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d8391-118">**IDebugShaderCallback**</span><span class="sxs-lookup"><span data-stu-id="d8391-118">**IDebugShaderCallback**</span></span>](/windows/desktop/direct3dtools/idebugshadercallback)

 

 
