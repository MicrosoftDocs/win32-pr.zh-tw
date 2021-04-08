---
title: IDRMStatusCallback OnStatus 方法
description: OnStatus 方法會從非同步 DRM 進程接收狀態訊息。
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus 方法 windows Media 格式
- OnStatus 方法 windows Media Format，IDRMStatusCallback 介面
- IDRMStatusCallback 介面 windows Media Format，OnStatus 方法
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022334"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="ef377-106">IDRMStatusCallback：： OnStatus 方法</span><span class="sxs-lookup"><span data-stu-id="ef377-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="ef377-107">**OnStatus** 方法會從非同步 DRM 進程接收狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="ef377-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef377-108">語法</span><span class="sxs-lookup"><span data-stu-id="ef377-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="ef377-109">參數</span><span class="sxs-lookup"><span data-stu-id="ef377-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef377-110">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef377-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef377-111">狀態碼。</span><span class="sxs-lookup"><span data-stu-id="ef377-111">Status code.</span></span> <span data-ttu-id="ef377-112">訊息碼是在 **MSDRM \_ 狀態** 列舉類型中定義。</span><span class="sxs-lookup"><span data-stu-id="ef377-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="ef377-113">*hr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef377-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef377-114">傳回支援狀態訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ef377-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="ef377-115">*dwType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef377-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef377-116">*PValue* 所指向之資料的類型。</span><span class="sxs-lookup"><span data-stu-id="ef377-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="ef377-117">設定為 [**DRM \_ ATTR \_ DATATYPE**](drm-attr-datatype.md) 列舉值的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ef377-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ef377-118">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef377-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef377-119">與狀態訊息相關之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="ef377-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="ef377-120">資料的類型取決於 *dwType* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="ef377-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="ef377-121">如需詳細資訊，請參閱 [**DRM \_ ATTR \_ DATATYPE**](drm-attr-datatype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="ef377-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ef377-122">*pvCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef377-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef377-123">選擇性參數，可用來識別傳送訊息的物件。</span><span class="sxs-lookup"><span data-stu-id="ef377-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="ef377-124">藉由在註冊此回呼時設定 *pvCoNtext* ，您可以使用相同的回呼來處理多個非同步處理常式。</span><span class="sxs-lookup"><span data-stu-id="ef377-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef377-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef377-125">Return value</span></span>

<span data-ttu-id="ef377-126">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ef377-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef377-127">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ef377-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef377-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ef377-128">Return code</span></span>                                                                          | <span data-ttu-id="ef377-129">Description</span><span class="sxs-lookup"><span data-stu-id="ef377-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ef377-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ef377-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ef377-131">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ef377-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef377-132">備註</span><span class="sxs-lookup"><span data-stu-id="ef377-132">Remarks</span></span>

<span data-ttu-id="ef377-133">無。</span><span class="sxs-lookup"><span data-stu-id="ef377-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef377-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef377-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef377-135">**DRM \_ ATTR \_ 資料類型**</span><span class="sxs-lookup"><span data-stu-id="ef377-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="ef377-136">**IDRMStatusCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="ef377-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





