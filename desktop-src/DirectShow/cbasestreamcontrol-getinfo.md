---
description: GetInfo 方法會抓取目前資料流程控制設定的相關資訊，包括開始和停止時間。 這個方法會實 IAMStreamControl：： GetInfo 方法。
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: 'CBaseStreamControl. GetInfo 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995034"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="6571b-104">CBaseStreamControl. GetInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6571b-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="6571b-105">方法會抓取 `GetInfo` 目前資料流程控制設定的相關資訊，包括開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="6571b-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="6571b-106">這個方法會實 [**IAMStreamControl：： GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="6571b-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6571b-107">語法</span><span class="sxs-lookup"><span data-stu-id="6571b-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6571b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6571b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6571b-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="6571b-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6571b-110">呼叫端所配置的 [**AM \_ 資料流程 \_ 資訊**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) 結構的指標，該結構會接收目前的資料流程控制設定。</span><span class="sxs-lookup"><span data-stu-id="6571b-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6571b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6571b-111">Return value</span></span>

<span data-ttu-id="6571b-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="6571b-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="6571b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6571b-113">Requirements</span></span>



| <span data-ttu-id="6571b-114">需求</span><span class="sxs-lookup"><span data-stu-id="6571b-114">Requirement</span></span> | <span data-ttu-id="6571b-115">值</span><span class="sxs-lookup"><span data-stu-id="6571b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6571b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="6571b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6571b-117"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6571b-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6571b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="6571b-118">Library</span></span><br/> | <dl> <span data-ttu-id="6571b-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6571b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6571b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6571b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6571b-121">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="6571b-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




