---
description: 當長條圖載入已完成時，用來通知主機的回呼函式。
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks：： LoadHistogramComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0e468422f722a8bd549d63f34225833462856b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970298"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span data-ttu-id="44348-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks：： LoadHistogramComplete 方法</span><span class="sxs-lookup"><span data-stu-id="44348-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadHistogramComplete method</span></span>

<span data-ttu-id="44348-104">當長條圖載入已完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="44348-104">A callback function used to notify the host when a histogram load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="44348-105">語法</span><span class="sxs-lookup"><span data-stu-id="44348-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="44348-106">參數</span><span class="sxs-lookup"><span data-stu-id="44348-106">Parameters</span></span>

<span data-ttu-id="44348-107">*長條圖* </span><span class="sxs-lookup"><span data-stu-id="44348-107">*histogram* </span></span>  
<span data-ttu-id="44348-108">已載入長條圖的長條圖資料位址。</span><span class="sxs-lookup"><span data-stu-id="44348-108">The address of histogram data for the loaded histogram.</span></span>

## <a name="return-value"></a><span data-ttu-id="44348-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="44348-109">Return value</span></span>

<span data-ttu-id="44348-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="44348-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44348-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="44348-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44348-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="44348-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="44348-113">標頭</span><span class="sxs-lookup"><span data-stu-id="44348-113">Header</span></span></p></td><td><span data-ttu-id="44348-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="44348-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="44348-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="44348-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="44348-116">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="44348-116">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
