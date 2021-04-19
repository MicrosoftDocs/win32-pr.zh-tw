---
description: Get \_ StreamTypeB 方法會抓取字串，表示目前資料流程的媒體類型 GUID。
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'IMediaDet：： get_StreamTypeB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993624"
---
# <a name="imediadetget_streamtypeb-method"></a><span data-ttu-id="18874-103">IMediaDet：： get \_ StreamTypeB 方法</span><span class="sxs-lookup"><span data-stu-id="18874-103">IMediaDet::get\_StreamTypeB method</span></span>

> [!Note]  
> <span data-ttu-id="18874-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="18874-104">\[Deprecated.</span></span> <span data-ttu-id="18874-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="18874-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="18874-106">方法會抓取 `get_StreamTypeB` 字串，表示目前資料流程之媒體類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="18874-106">The `get_StreamTypeB` method retrieves a string representing the GUID of the media type for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="18874-107">語法</span><span class="sxs-lookup"><span data-stu-id="18874-107">Syntax</span></span>


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="18874-108">參數</span><span class="sxs-lookup"><span data-stu-id="18874-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18874-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="18874-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="18874-110">接收媒體類型 GUID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="18874-110">Receives a string representation of the media type GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18874-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="18874-111">Return value</span></span>

<span data-ttu-id="18874-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="18874-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18874-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="18874-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18874-114">備註</span><span class="sxs-lookup"><span data-stu-id="18874-114">Remarks</span></span>

<span data-ttu-id="18874-115">傳回的 **BSTR** 格式如下所示： `{73647561-0000-0010-8000-00AA00389B71}`</span><span class="sxs-lookup"><span data-stu-id="18874-115">The returned **BSTR** is formatted like the following: `{73647561-0000-0010-8000-00AA00389B71}`</span></span>

<span data-ttu-id="18874-116">方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="18874-116">The method allocates memory for the string.</span></span> <span data-ttu-id="18874-117">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="18874-117">The application must call **SysFreeString** to free the memory.</span></span>

<span data-ttu-id="18874-118">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="18874-118">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="18874-119">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="18874-119">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="18874-120">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="18874-120">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="18874-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="18874-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="18874-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="18874-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="18874-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="18874-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18874-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="18874-124">Requirements</span></span>



| <span data-ttu-id="18874-125">需求</span><span class="sxs-lookup"><span data-stu-id="18874-125">Requirement</span></span> | <span data-ttu-id="18874-126">值</span><span class="sxs-lookup"><span data-stu-id="18874-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18874-127">標頭</span><span class="sxs-lookup"><span data-stu-id="18874-127">Header</span></span><br/>  | <dl> <span data-ttu-id="18874-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="18874-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="18874-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="18874-129">Library</span></span><br/> | <dl> <span data-ttu-id="18874-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="18874-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18874-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18874-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18874-132">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="18874-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="18874-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="18874-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




