---
description: GetConnectedMediaType 方法會在範例提取的輸入 pin 上抓取連接的媒體類型。
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'ISampleGrabber：： GetConnectedMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992553"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="5a3cc-103">ISampleGrabber：： GetConnectedMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="5a3cc-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="5a3cc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-104">\[Deprecated.</span></span> <span data-ttu-id="5a3cc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5a3cc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a3cc-106">`GetConnectedMediaType`方法會在範例提取的輸入釘選上抓取連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3cc-107">語法</span><span class="sxs-lookup"><span data-stu-id="5a3cc-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="5a3cc-108">參數</span><span class="sxs-lookup"><span data-stu-id="5a3cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3cc-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="5a3cc-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3cc-110">由呼叫端配置的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3cc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a3cc-111">Return value</span></span>

<span data-ttu-id="5a3cc-112">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-112">Returns one of the following values.</span></span>



| <span data-ttu-id="5a3cc-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5a3cc-113">Return code</span></span>                                                                                           | <span data-ttu-id="5a3cc-114">Description</span><span class="sxs-lookup"><span data-stu-id="5a3cc-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="5a3cc-115"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3cc-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5a3cc-116">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="5a3cc-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3cc-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="5a3cc-118">成功。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="5a3cc-119"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3cc-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5a3cc-120">篩選未連接。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a3cc-121">備註</span><span class="sxs-lookup"><span data-stu-id="5a3cc-121">Remarks</span></span>

<span data-ttu-id="5a3cc-122">這個方法會將媒體類型複製到 *pType* 所指定的 **AM \_ 媒體 \_ 類型** 結構中。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="5a3cc-123">呼叫端必須釋放媒體類型的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="5a3cc-124">您可以使用 **CoTaskMemFree** 函式，或基類程式庫中的 [**FreeMediaType**](freemediatype.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="5a3cc-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a3cc-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a3cc-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5a3cc-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a3cc-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a3cc-128">Requirements</span></span>



| <span data-ttu-id="5a3cc-129">需求</span><span class="sxs-lookup"><span data-stu-id="5a3cc-129">Requirement</span></span> | <span data-ttu-id="5a3cc-130">值</span><span class="sxs-lookup"><span data-stu-id="5a3cc-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3cc-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5a3cc-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5a3cc-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3cc-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5a3cc-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a3cc-133">Library</span></span><br/> | <dl> <span data-ttu-id="5a3cc-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a3cc-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3cc-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a3cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3cc-136">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="5a3cc-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="5a3cc-137">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="5a3cc-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




