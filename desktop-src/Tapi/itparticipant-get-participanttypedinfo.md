---
description: Get \_ ParticipantTypedInfo 方法會取得所需資訊類型的 BSTR 標記法，例如 PTI \_ EMAILADDRESS。
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'ITParticipant：： get_ParticipantTypedInfo 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989499"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="f6e35-103">ITParticipant：： get \_ ParticipantTypedInfo 方法</span><span class="sxs-lookup"><span data-stu-id="f6e35-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="f6e35-104">\[**取得 \_ParticipantTypedInfo** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f6e35-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6e35-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f6e35-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6e35-106">**Get \_ ParticipantTypedInfo** 方法會取得所需資訊類型的 **BSTR** 標記法，例如 PTI \_ EMAILADDRESS。</span><span class="sxs-lookup"><span data-stu-id="f6e35-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e35-107">語法</span><span class="sxs-lookup"><span data-stu-id="f6e35-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f6e35-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6e35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e35-109">*InfoType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6e35-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e35-110">[**參與者 \_所 \_**](participant-typed-info.md) 需資訊類型的類型資訊描述元。</span><span class="sxs-lookup"><span data-stu-id="f6e35-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="f6e35-111">*ppInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6e35-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e35-112">所需資訊的 **BSTR** 標記法指標。</span><span class="sxs-lookup"><span data-stu-id="f6e35-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6e35-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6e35-113">Return value</span></span>

<span data-ttu-id="f6e35-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f6e35-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f6e35-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f6e35-115">Return code</span></span>                                                                                    | <span data-ttu-id="f6e35-116">Description</span><span class="sxs-lookup"><span data-stu-id="f6e35-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f6e35-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="f6e35-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="f6e35-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f6e35-119"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="f6e35-120">將資訊儲存到 *ppInfo* 失敗。</span><span class="sxs-lookup"><span data-stu-id="f6e35-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="f6e35-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="f6e35-122">*InfoType* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f6e35-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="f6e35-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="f6e35-124">*PpInfo* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="f6e35-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="f6e35-125"><dt>**TAPI \_ E \_ NOITEM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="f6e35-126">TAPI 沒有指定類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="f6e35-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="f6e35-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="f6e35-128">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="f6e35-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6e35-129">備註</span><span class="sxs-lookup"><span data-stu-id="f6e35-129">Remarks</span></span>

<span data-ttu-id="f6e35-130">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppInfo* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f6e35-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e35-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6e35-131">Requirements</span></span>



| <span data-ttu-id="f6e35-132">需求</span><span class="sxs-lookup"><span data-stu-id="f6e35-132">Requirement</span></span> | <span data-ttu-id="f6e35-133">值</span><span class="sxs-lookup"><span data-stu-id="f6e35-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e35-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f6e35-134">TAPI version</span></span><br/> | <span data-ttu-id="f6e35-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f6e35-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="f6e35-136">標頭</span><span class="sxs-lookup"><span data-stu-id="f6e35-136">Header</span></span><br/>       | <dl> <span data-ttu-id="f6e35-137"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6e35-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="f6e35-138">Library</span></span><br/>      | <dl> <span data-ttu-id="f6e35-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f6e35-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f6e35-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6e35-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6e35-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6e35-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6e35-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e35-143">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="f6e35-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="f6e35-144">**參與者 \_ 輸入 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f6e35-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="f6e35-145">**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="f6e35-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

