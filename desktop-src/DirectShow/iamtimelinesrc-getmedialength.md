---
description: GetMediaLength 方法會抓取此來源物件的媒體長度。
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'IAMTimelineSrc：： GetMediaLength 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977561"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="eed0b-103">IAMTimelineSrc：： GetMediaLength 方法</span><span class="sxs-lookup"><span data-stu-id="eed0b-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="eed0b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="eed0b-104">\[Deprecated.</span></span> <span data-ttu-id="eed0b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="eed0b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eed0b-106">方法會抓取 `GetMediaLength` 此來源物件的媒體長度。</span><span class="sxs-lookup"><span data-stu-id="eed0b-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed0b-107">語法</span><span class="sxs-lookup"><span data-stu-id="eed0b-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="eed0b-108">參數</span><span class="sxs-lookup"><span data-stu-id="eed0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed0b-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="eed0b-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="eed0b-110">以 100-毫微秒單位接收媒體長度。</span><span class="sxs-lookup"><span data-stu-id="eed0b-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed0b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eed0b-111">Return value</span></span>

<span data-ttu-id="eed0b-112">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="eed0b-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="eed0b-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eed0b-113">Return code</span></span>                                                                                     | <span data-ttu-id="eed0b-114">Description</span><span class="sxs-lookup"><span data-stu-id="eed0b-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="eed0b-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eed0b-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="eed0b-116">成功。</span><span class="sxs-lookup"><span data-stu-id="eed0b-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="eed0b-117"><dt>**E \_ NOTDETERMINED**</dt></span><span class="sxs-lookup"><span data-stu-id="eed0b-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="eed0b-118">未在這個物件上設定媒體時間。</span><span class="sxs-lookup"><span data-stu-id="eed0b-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="eed0b-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="eed0b-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="eed0b-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="eed0b-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="eed0b-121">備註</span><span class="sxs-lookup"><span data-stu-id="eed0b-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eed0b-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="eed0b-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eed0b-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="eed0b-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eed0b-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="eed0b-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eed0b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="eed0b-125">Requirements</span></span>



| <span data-ttu-id="eed0b-126">需求</span><span class="sxs-lookup"><span data-stu-id="eed0b-126">Requirement</span></span> | <span data-ttu-id="eed0b-127">值</span><span class="sxs-lookup"><span data-stu-id="eed0b-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eed0b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="eed0b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="eed0b-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="eed0b-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eed0b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="eed0b-130">Library</span></span><br/> | <dl> <span data-ttu-id="eed0b-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eed0b-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed0b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eed0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed0b-133">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="eed0b-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="eed0b-134">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="eed0b-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="eed0b-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="eed0b-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




