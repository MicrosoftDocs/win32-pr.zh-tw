---
description: 多媒體串流錯誤和成功碼
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: 多媒體串流錯誤和成功碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321655"
---
# <a name="multimedia-streaming-error-and-success-codes"></a><span data-ttu-id="2e5b2-103">多媒體串流錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2e5b2-103">Multimedia Streaming Error and Success Codes</span></span>

> [!Note]  
> <span data-ttu-id="2e5b2-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-104">This API is deprecated.</span></span> <span data-ttu-id="2e5b2-105">新的應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-105">New applications should not use it.</span></span>

 

<span data-ttu-id="2e5b2-106">下列清單包含使用多媒體串流介面的應用程式的錯誤訊息和成功通知。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-106">The following list contains error messages and success notifications for applications that use the multimedia streaming interfaces.</span></span> <span data-ttu-id="2e5b2-107">這份清單不包含所有可能的錯誤;所顯示的錯誤特別適用于 Microsoft® DirectShow®多媒體串流介面的執行。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-107">This list does not contain all possible errors; the errors shown apply specifically to the Microsoft® DirectShow® implementation of the multimedia streaming interfaces.</span></span>



| <span data-ttu-id="2e5b2-108">值</span><span class="sxs-lookup"><span data-stu-id="2e5b2-108">Value</span></span>                       | <span data-ttu-id="2e5b2-109">十六進位碼</span><span class="sxs-lookup"><span data-stu-id="2e5b2-109">Hexadecimal code</span></span> | <span data-ttu-id="2e5b2-110">Description</span><span class="sxs-lookup"><span data-stu-id="2e5b2-110">Description</span></span>                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5b2-111">MS \_ S \_ 暫止</span><span class="sxs-lookup"><span data-stu-id="2e5b2-111">MS\_S\_PENDING</span></span>              | <span data-ttu-id="2e5b2-112">0x00040001</span><span class="sxs-lookup"><span data-stu-id="2e5b2-112">0x00040001</span></span>       | <span data-ttu-id="2e5b2-113">範例更新尚未完成。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-113">Sample update is not yet complete.</span></span>                                                                                                                                                         |
| <span data-ttu-id="2e5b2-114">MS \_ S \_ NOUPDATE</span><span class="sxs-lookup"><span data-stu-id="2e5b2-114">MS\_S\_NOUPDATE</span></span>             | <span data-ttu-id="2e5b2-115">0x00040002</span><span class="sxs-lookup"><span data-stu-id="2e5b2-115">0x00040002</span></span>       | <span data-ttu-id="2e5b2-116">未在強制完成後更新範例。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-116">Sample was not updated after forced completion.</span></span>                                                                                                                                            |
| <span data-ttu-id="2e5b2-117">MS \_ S \_ ENDOFSTREAM</span><span class="sxs-lookup"><span data-stu-id="2e5b2-117">MS\_S\_ENDOFSTREAM</span></span>          | <span data-ttu-id="2e5b2-118">0x00040003</span><span class="sxs-lookup"><span data-stu-id="2e5b2-118">0x00040003</span></span>       | <span data-ttu-id="2e5b2-119">資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-119">End of stream.</span></span> <span data-ttu-id="2e5b2-120">範例未更新。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-120">Sample not updated.</span></span>                                                                                                                                                         |
| <span data-ttu-id="2e5b2-121">MS \_ E \_ SAMPLEALLOC</span><span class="sxs-lookup"><span data-stu-id="2e5b2-121">MS\_E\_SAMPLEALLOC</span></span>          | <span data-ttu-id="2e5b2-122">0x80040401</span><span class="sxs-lookup"><span data-stu-id="2e5b2-122">0x80040401</span></span>       | <span data-ttu-id="2e5b2-123">無法從 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)物件移除 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)物件，因為它仍包含至少一個已配置的範例。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-123">An [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) object could not be removed from an [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) object because it still contains at least one allocated sample.</span></span> |
| <span data-ttu-id="2e5b2-124">MS \_ E \_ PURPOSEID</span><span class="sxs-lookup"><span data-stu-id="2e5b2-124">MS\_E\_PURPOSEID</span></span>            | <span data-ttu-id="2e5b2-125">0x80040402</span><span class="sxs-lookup"><span data-stu-id="2e5b2-125">0x80040402</span></span>       | <span data-ttu-id="2e5b2-126">指定的目的識別碼無法用於呼叫。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-126">The specified purpose ID can't be used for the call.</span></span>                                                                                                                                       |
| <span data-ttu-id="2e5b2-127">MS \_ E \_ NOSTREAM</span><span class="sxs-lookup"><span data-stu-id="2e5b2-127">MS\_E\_NOSTREAM</span></span>             | <span data-ttu-id="2e5b2-128">0x80040403</span><span class="sxs-lookup"><span data-stu-id="2e5b2-128">0x80040403</span></span>       | <span data-ttu-id="2e5b2-129">找不到具有指定屬性的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-129">No stream can be found with the specified attributes.</span></span>                                                                                                                                      |
| <span data-ttu-id="2e5b2-130">MS \_ E \_ NOSEEKING</span><span class="sxs-lookup"><span data-stu-id="2e5b2-130">MS\_E\_NOSEEKING</span></span>            | <span data-ttu-id="2e5b2-131">0x80040404</span><span class="sxs-lookup"><span data-stu-id="2e5b2-131">0x80040404</span></span>       | <span data-ttu-id="2e5b2-132">這個 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 物件不支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-132">Seeking not supported for this [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) object.</span></span>                                                                                                      |
| <span data-ttu-id="2e5b2-133">MS \_ E \_ 不相容</span><span class="sxs-lookup"><span data-stu-id="2e5b2-133">MS\_E\_INCOMPATIBLE</span></span>         | <span data-ttu-id="2e5b2-134">0x80040405</span><span class="sxs-lookup"><span data-stu-id="2e5b2-134">0x80040405</span></span>       | <span data-ttu-id="2e5b2-135">資料流程格式不相容。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-135">The stream formats are not compatible.</span></span>                                                                                                                                                     |
| <span data-ttu-id="2e5b2-136">MS \_ E \_ 忙碌</span><span class="sxs-lookup"><span data-stu-id="2e5b2-136">MS\_E\_BUSY</span></span>                 | <span data-ttu-id="2e5b2-137">0x80040406</span><span class="sxs-lookup"><span data-stu-id="2e5b2-137">0x80040406</span></span>       | <span data-ttu-id="2e5b2-138">此範例忙碌中。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-138">The sample is busy.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="2e5b2-139">MS \_ E \_ NOTINIT</span><span class="sxs-lookup"><span data-stu-id="2e5b2-139">MS\_E\_NOTINIT</span></span>              | <span data-ttu-id="2e5b2-140">0x80040407</span><span class="sxs-lookup"><span data-stu-id="2e5b2-140">0x80040407</span></span>       | <span data-ttu-id="2e5b2-141">物件無法接受呼叫，因為未呼叫其 initialize 函數或對等專案。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-141">The object can't accept the call because its initialize function or equivalent has not been called.</span></span>                                                                                        |
| <span data-ttu-id="2e5b2-142">MS \_ E \_ SOURCEALREADYDEFINED</span><span class="sxs-lookup"><span data-stu-id="2e5b2-142">MS\_E\_SOURCEALREADYDEFINED</span></span> | <span data-ttu-id="2e5b2-143">0x80040408</span><span class="sxs-lookup"><span data-stu-id="2e5b2-143">0x80040408</span></span>       | <span data-ttu-id="2e5b2-144">來源已定義。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-144">Source already defined.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="2e5b2-145">MS \_ E \_ INVALIDSTREAMTYPE</span><span class="sxs-lookup"><span data-stu-id="2e5b2-145">MS\_E\_INVALIDSTREAMTYPE</span></span>    | <span data-ttu-id="2e5b2-146">0x80040409</span><span class="sxs-lookup"><span data-stu-id="2e5b2-146">0x80040409</span></span>       | <span data-ttu-id="2e5b2-147">資料流程類型對這項作業無效。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-147">The stream type is not valid for this operation.</span></span>                                                                                                                                           |
| <span data-ttu-id="2e5b2-148">MS \_ E \_ NOTRUNNING</span><span class="sxs-lookup"><span data-stu-id="2e5b2-148">MS\_E\_NOTRUNNING</span></span>           | <span data-ttu-id="2e5b2-149">0x8004040A</span><span class="sxs-lookup"><span data-stu-id="2e5b2-149">0x8004040A</span></span>       | <span data-ttu-id="2e5b2-150">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)物件未處於執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="2e5b2-150">The [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) object is not in running state.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="2e5b2-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e5b2-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e5b2-152">多媒體串流</span><span class="sxs-lookup"><span data-stu-id="2e5b2-152">Multimedia Streaming</span></span>](multimedia-streaming.md)
</dt> </dl>

 

 



