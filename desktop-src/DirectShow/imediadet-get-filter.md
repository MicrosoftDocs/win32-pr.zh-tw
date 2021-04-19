---
description: Get \_ 篩選方法會抓取媒體偵測器目前所使用的來源篩選指標。
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'IMediaDet：： get_Filter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984387"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="b9e71-103">IMediaDet：： get \_ Filter 方法</span><span class="sxs-lookup"><span data-stu-id="b9e71-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="b9e71-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b9e71-104">\[Deprecated.</span></span> <span data-ttu-id="b9e71-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b9e71-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b9e71-106">方法會抓取 `get_Filter` 媒體偵測器目前所使用的來源篩選指標。</span><span class="sxs-lookup"><span data-stu-id="b9e71-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e71-107">語法</span><span class="sxs-lookup"><span data-stu-id="b9e71-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="b9e71-108">參數</span><span class="sxs-lookup"><span data-stu-id="b9e71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e71-109">*ppVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="b9e71-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e71-110">接收篩選的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b9e71-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="b9e71-111">如果沒有來源篩選正在使用中，此值會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b9e71-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e71-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9e71-112">Return value</span></span>

<span data-ttu-id="b9e71-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b9e71-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9e71-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b9e71-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e71-115">備註</span><span class="sxs-lookup"><span data-stu-id="b9e71-115">Remarks</span></span>

<span data-ttu-id="b9e71-116">當此方法傳回時，如果 *\* ppVal* 不是 **Null**，則 **IUnknown** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="b9e71-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="b9e71-117">使用完畢後，請釋放介面。</span><span class="sxs-lookup"><span data-stu-id="b9e71-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="b9e71-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b9e71-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9e71-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b9e71-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b9e71-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b9e71-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b9e71-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9e71-121">Requirements</span></span>



| <span data-ttu-id="b9e71-122">需求</span><span class="sxs-lookup"><span data-stu-id="b9e71-122">Requirement</span></span> | <span data-ttu-id="b9e71-123">值</span><span class="sxs-lookup"><span data-stu-id="b9e71-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e71-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b9e71-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b9e71-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e71-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b9e71-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9e71-126">Library</span></span><br/> | <dl> <span data-ttu-id="b9e71-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9e71-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e71-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9e71-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e71-129">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="b9e71-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="b9e71-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b9e71-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




