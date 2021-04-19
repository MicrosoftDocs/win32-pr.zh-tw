---
description: SetMediaLength 方法會指定原始程式檔的持續時間。
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'IAMTimelineSrc：： SetMediaLength 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995484"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="4edcc-103">IAMTimelineSrc：： SetMediaLength 方法</span><span class="sxs-lookup"><span data-stu-id="4edcc-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="4edcc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4edcc-104">\[Deprecated.</span></span> <span data-ttu-id="4edcc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4edcc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4edcc-106">方法會指定原始程式檔的 `SetMediaLength` 持續時間。</span><span class="sxs-lookup"><span data-stu-id="4edcc-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4edcc-107">語法</span><span class="sxs-lookup"><span data-stu-id="4edcc-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="4edcc-108">參數</span><span class="sxs-lookup"><span data-stu-id="4edcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4edcc-109">*長度*</span><span class="sxs-lookup"><span data-stu-id="4edcc-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="4edcc-110">媒體長度，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="4edcc-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4edcc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4edcc-111">Return value</span></span>

<span data-ttu-id="4edcc-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4edcc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4edcc-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4edcc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4edcc-114">備註</span><span class="sxs-lookup"><span data-stu-id="4edcc-114">Remarks</span></span>

<span data-ttu-id="4edcc-115">您可以在設定媒體停止時間之前設定媒體長度，以避免潛在的轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="4edcc-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="4edcc-116">當您設定 media stop time 時，DES 會根據媒體長度來檢查它。</span><span class="sxs-lookup"><span data-stu-id="4edcc-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="4edcc-117">這個方法不會驗證 *長度* 參數，但值必須等於原始程式檔的實際持續時間。</span><span class="sxs-lookup"><span data-stu-id="4edcc-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="4edcc-118">藉由呼叫 [**IMediaDet：： get \_ StreamLength**](imediadet-get-streamlength.md)來取得來源檔案持續時間。</span><span class="sxs-lookup"><span data-stu-id="4edcc-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="4edcc-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4edcc-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4edcc-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4edcc-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4edcc-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4edcc-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4edcc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4edcc-122">Requirements</span></span>



| <span data-ttu-id="4edcc-123">需求</span><span class="sxs-lookup"><span data-stu-id="4edcc-123">Requirement</span></span> | <span data-ttu-id="4edcc-124">值</span><span class="sxs-lookup"><span data-stu-id="4edcc-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4edcc-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4edcc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4edcc-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4edcc-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4edcc-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="4edcc-127">Library</span></span><br/> | <dl> <span data-ttu-id="4edcc-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4edcc-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4edcc-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4edcc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edcc-130">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="4edcc-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4edcc-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4edcc-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




