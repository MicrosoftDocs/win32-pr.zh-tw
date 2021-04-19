---
description: GetStreamCaps 方法會取得與指定之格式索引相關聯的功能。
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'ITFormatControl：： GetStreamCaps 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000415"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="50494-103">ITFormatControl：： GetStreamCaps 方法</span><span class="sxs-lookup"><span data-stu-id="50494-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="50494-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="50494-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50494-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="50494-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="50494-106">**GetStreamCaps** 方法會取得與指定之格式索引相關聯的功能。</span><span class="sxs-lookup"><span data-stu-id="50494-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="50494-107">語法</span><span class="sxs-lookup"><span data-stu-id="50494-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="50494-108">參數</span><span class="sxs-lookup"><span data-stu-id="50494-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50494-109">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50494-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50494-110">正在探查之格式的索引。</span><span class="sxs-lookup"><span data-stu-id="50494-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="50494-111">*ppMediaType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50494-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50494-112">終端機格式的 **AM \_ 媒體 \_ 類型** 描述元指標。</span><span class="sxs-lookup"><span data-stu-id="50494-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="50494-113">如需 **\_ 媒體 \_ 類型** 的詳細資訊，請參閱 DirectX 檔。</span><span class="sxs-lookup"><span data-stu-id="50494-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="50494-114">*pStreamConfigCaps* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50494-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50494-115">提供有關資料流程功能詳細資訊的 [**TAPI \_ 串流設定 \_ \_ cap**](tapi-stream-config-caps.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="50494-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="50494-116">*pfEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50494-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50494-117">指出是否已啟用與目前索引相關聯的格式。</span><span class="sxs-lookup"><span data-stu-id="50494-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50494-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="50494-118">Return value</span></span>

<span data-ttu-id="50494-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="50494-119">This method can return one of these values.</span></span>



| <span data-ttu-id="50494-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="50494-120">Return code</span></span>                                                                                   | <span data-ttu-id="50494-121">Description</span><span class="sxs-lookup"><span data-stu-id="50494-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="50494-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="50494-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="50494-123">方法成功。</span><span class="sxs-lookup"><span data-stu-id="50494-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="50494-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="50494-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="50494-125">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="50494-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50494-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="50494-126">Requirements</span></span>



| <span data-ttu-id="50494-127">需求</span><span class="sxs-lookup"><span data-stu-id="50494-127">Requirement</span></span> | <span data-ttu-id="50494-128">值</span><span class="sxs-lookup"><span data-stu-id="50494-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50494-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="50494-129">TAPI version</span></span><br/> | <span data-ttu-id="50494-130">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="50494-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="50494-131">標頭</span><span class="sxs-lookup"><span data-stu-id="50494-131">Header</span></span><br/>       | <dl> <span data-ttu-id="50494-132"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="50494-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50494-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="50494-133">Library</span></span><br/>      | <dl> <span data-ttu-id="50494-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="50494-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="50494-135">DLL</span><span class="sxs-lookup"><span data-stu-id="50494-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="50494-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50494-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50494-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50494-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50494-138">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="50494-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="50494-139">**TAPI \_ 串流 \_ 設定 \_ CAP**</span><span class="sxs-lookup"><span data-stu-id="50494-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




