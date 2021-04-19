---
description: 使用指定的初始化資料和自訂資料，建立媒體金鑰會話物件。 .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: IMFMediaKeys：： CreateSession 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993788"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="95ee9-104">IMFMediaKeys：： CreateSession 方法</span><span class="sxs-lookup"><span data-stu-id="95ee9-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="95ee9-105">使用指定的初始化資料和自訂資料，建立媒體金鑰會話物件。</span><span class="sxs-lookup"><span data-stu-id="95ee9-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="95ee9-106">.</span><span class="sxs-lookup"><span data-stu-id="95ee9-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ee9-107">語法</span><span class="sxs-lookup"><span data-stu-id="95ee9-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="95ee9-108">參數</span><span class="sxs-lookup"><span data-stu-id="95ee9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ee9-109">*mimeType*</span><span class="sxs-lookup"><span data-stu-id="95ee9-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-110">用於內容之媒體容器的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="95ee9-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="95ee9-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="95ee9-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-112">金鑰系統的初始化資料。</span><span class="sxs-lookup"><span data-stu-id="95ee9-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="95ee9-113">*Cb*</span><span class="sxs-lookup"><span data-stu-id="95ee9-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-114">*InitData* 的計數（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95ee9-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="95ee9-115">*customData*</span><span class="sxs-lookup"><span data-stu-id="95ee9-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-116">傳送至金鑰系統的自訂資料。</span><span class="sxs-lookup"><span data-stu-id="95ee9-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="95ee9-117">*cbCustomData*</span><span class="sxs-lookup"><span data-stu-id="95ee9-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-118">*CbCustomData* 的計數（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95ee9-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="95ee9-119">*通知*</span><span class="sxs-lookup"><span data-stu-id="95ee9-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-120">通知</span><span class="sxs-lookup"><span data-stu-id="95ee9-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="95ee9-121">*ppSession*</span><span class="sxs-lookup"><span data-stu-id="95ee9-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="95ee9-122">媒體金鑰會話。</span><span class="sxs-lookup"><span data-stu-id="95ee9-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ee9-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="95ee9-123">Return value</span></span>

<span data-ttu-id="95ee9-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="95ee9-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95ee9-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="95ee9-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ee9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="95ee9-126">Requirements</span></span>



| <span data-ttu-id="95ee9-127">需求</span><span class="sxs-lookup"><span data-stu-id="95ee9-127">Requirement</span></span> | <span data-ttu-id="95ee9-128">值</span><span class="sxs-lookup"><span data-stu-id="95ee9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ee9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95ee9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="95ee9-130">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95ee9-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="95ee9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95ee9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="95ee9-132">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95ee9-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="95ee9-133">Idl</span><span class="sxs-lookup"><span data-stu-id="95ee9-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95ee9-134"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="95ee9-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95ee9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95ee9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ee9-136">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="95ee9-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




