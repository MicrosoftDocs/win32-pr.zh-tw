---
description: 當材質值讀取完成時，用來通知主機的回呼函數。
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks：： ReadTexelValueComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7069d286cf65d87ba7bf4c576de3692b2a51d1a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510136"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span data-ttu-id="1da8c-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks：： ReadTexelValueComplete 方法</span><span class="sxs-lookup"><span data-stu-id="1da8c-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks::ReadTexelValueComplete method</span></span>

<span data-ttu-id="1da8c-104">當材質值讀取完成時，用來通知主機的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1da8c-104">A callback function used to notify the host when a texel value read has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da8c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1da8c-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a><span data-ttu-id="1da8c-106">參數</span><span class="sxs-lookup"><span data-stu-id="1da8c-106">Parameters</span></span>

<span data-ttu-id="1da8c-107">*numChannels* </span><span class="sxs-lookup"><span data-stu-id="1da8c-107">*numChannels* </span></span>  
<span data-ttu-id="1da8c-108">材質具有的通道數目。</span><span class="sxs-lookup"><span data-stu-id="1da8c-108">The number of channels the texel has.</span></span>

<span data-ttu-id="1da8c-109">*count0 \_ channelNames* </span><span class="sxs-lookup"><span data-stu-id="1da8c-109">*count0\_channelNames* </span></span>  
<span data-ttu-id="1da8c-110">包含通道名稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="1da8c-110">COM strings containing the names of the channels.</span></span>

<span data-ttu-id="1da8c-111">*count0 \_ channelValues* </span><span class="sxs-lookup"><span data-stu-id="1da8c-111">*count0\_channelValues* </span></span>  
<span data-ttu-id="1da8c-112">通道的值。</span><span class="sxs-lookup"><span data-stu-id="1da8c-112">The values of the channels.</span></span>

## <a name="return-value"></a><span data-ttu-id="1da8c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1da8c-113">Return value</span></span>

<span data-ttu-id="1da8c-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1da8c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1da8c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1da8c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da8c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1da8c-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1da8c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1da8c-117">Header</span></span></p></td><td><span data-ttu-id="1da8c-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1da8c-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1da8c-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="1da8c-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1da8c-120">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="1da8c-120">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
