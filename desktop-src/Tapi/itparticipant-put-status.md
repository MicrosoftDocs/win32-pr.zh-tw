---
description: Put \_ status 方法會設定參與者的狀態。
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant：:p ut_Status 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994288"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="68169-103">ITParticipant：:p 的內容 \_ 狀態方法</span><span class="sxs-lookup"><span data-stu-id="68169-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="68169-104">\[**put \_** 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用狀態。</span><span class="sxs-lookup"><span data-stu-id="68169-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68169-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="68169-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68169-106">**Put \_ status** 方法會設定參與者的狀態。</span><span class="sxs-lookup"><span data-stu-id="68169-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="68169-107">語法</span><span class="sxs-lookup"><span data-stu-id="68169-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="68169-108">參數</span><span class="sxs-lookup"><span data-stu-id="68169-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68169-109">*pITStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68169-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68169-110">[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="68169-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="68169-111">*fEnable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68169-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68169-112">\_如果在資料流程上啟用參與者，則為 variant TRUE， \_ 如果要停用則為 variant。</span><span class="sxs-lookup"><span data-stu-id="68169-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68169-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="68169-113">Return value</span></span>

<span data-ttu-id="68169-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="68169-114">This method can return one of these values.</span></span>



| <span data-ttu-id="68169-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="68169-115">Return code</span></span>                                                                                   | <span data-ttu-id="68169-116">Description</span><span class="sxs-lookup"><span data-stu-id="68169-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68169-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="68169-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68169-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="68169-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="68169-119"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="68169-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="68169-120">未執行方法。</span><span class="sxs-lookup"><span data-stu-id="68169-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="68169-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="68169-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="68169-122">*PITStream* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="68169-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="68169-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="68169-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="68169-124">*PITStream* 參數未指向有效的介面。</span><span class="sxs-lookup"><span data-stu-id="68169-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="68169-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="68169-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68169-126">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="68169-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="68169-127">備註</span><span class="sxs-lookup"><span data-stu-id="68169-127">Remarks</span></span>

<span data-ttu-id="68169-128">啟用或停用某個參與者在資料流程上的狀態，可讓應用程式基本上將指定的參與者靜音。</span><span class="sxs-lookup"><span data-stu-id="68169-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="68169-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="68169-129">Requirements</span></span>



| <span data-ttu-id="68169-130">需求</span><span class="sxs-lookup"><span data-stu-id="68169-130">Requirement</span></span> | <span data-ttu-id="68169-131">值</span><span class="sxs-lookup"><span data-stu-id="68169-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68169-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="68169-132">TAPI version</span></span><br/> | <span data-ttu-id="68169-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="68169-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="68169-134">標頭</span><span class="sxs-lookup"><span data-stu-id="68169-134">Header</span></span><br/>       | <dl> <span data-ttu-id="68169-135"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="68169-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="68169-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="68169-136">Library</span></span><br/>      | <dl> <span data-ttu-id="68169-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="68169-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="68169-138">DLL</span><span class="sxs-lookup"><span data-stu-id="68169-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="68169-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68169-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68169-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68169-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68169-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="68169-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="68169-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="68169-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="68169-143">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="68169-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

