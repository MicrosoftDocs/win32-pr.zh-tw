---
description: Get \_ MediaTypes 方法會取得與參與者相關聯的媒體類型。
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'ITParticipant：： get_MediaTypes 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985537"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="23bb7-103">ITParticipant：： get \_ MediaTypes 方法</span><span class="sxs-lookup"><span data-stu-id="23bb7-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="23bb7-104">\[**取得 \_MediaTypes** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="23bb7-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="23bb7-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="23bb7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="23bb7-106">**Get \_ MediaTypes** 方法會取得與參與者相關聯的 [**媒體類型**](tapimediatype--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="23bb7-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="23bb7-107">語法</span><span class="sxs-lookup"><span data-stu-id="23bb7-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="23bb7-108">參數</span><span class="sxs-lookup"><span data-stu-id="23bb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23bb7-109">*plMediaType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="23bb7-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23bb7-110">媒體類型旗標的指標，例如 TAPIMEDIATYPE \_ VIDEO。</span><span class="sxs-lookup"><span data-stu-id="23bb7-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23bb7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="23bb7-111">Return value</span></span>

<span data-ttu-id="23bb7-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="23bb7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="23bb7-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="23bb7-113">Return code</span></span>                                                                                   | <span data-ttu-id="23bb7-114">Description</span><span class="sxs-lookup"><span data-stu-id="23bb7-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="23bb7-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="23bb7-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="23bb7-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="23bb7-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="23bb7-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="23bb7-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="23bb7-118">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="23bb7-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="23bb7-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="23bb7-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="23bb7-120">*PlMediaType* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="23bb7-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="23bb7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="23bb7-121">Requirements</span></span>



| <span data-ttu-id="23bb7-122">需求</span><span class="sxs-lookup"><span data-stu-id="23bb7-122">Requirement</span></span> | <span data-ttu-id="23bb7-123">值</span><span class="sxs-lookup"><span data-stu-id="23bb7-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23bb7-124">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="23bb7-124">TAPI version</span></span><br/> | <span data-ttu-id="23bb7-125">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="23bb7-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="23bb7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="23bb7-126">Header</span></span><br/>       | <dl> <span data-ttu-id="23bb7-127"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="23bb7-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="23bb7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="23bb7-128">Library</span></span><br/>      | <dl> <span data-ttu-id="23bb7-129"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="23bb7-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="23bb7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="23bb7-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="23bb7-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23bb7-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23bb7-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23bb7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23bb7-133">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="23bb7-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="23bb7-134">**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="23bb7-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




