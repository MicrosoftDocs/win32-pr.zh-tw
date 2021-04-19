---
description: 查詢 DirectX Video 加速 (DXVA) 解碼介面的讀取/寫入狀態。
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9：： QueryStatus 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977190"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="01fe8-103">IDirect3DDXVADevice9：： QueryStatus 方法</span><span class="sxs-lookup"><span data-stu-id="01fe8-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="01fe8-104">查詢 DirectX Video 加速 (DXVA) 解碼介面的讀取/寫入狀態。</span><span class="sxs-lookup"><span data-stu-id="01fe8-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="01fe8-105">語法</span><span class="sxs-lookup"><span data-stu-id="01fe8-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="01fe8-106">參數</span><span class="sxs-lookup"><span data-stu-id="01fe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fe8-107">*pSurface*</span><span class="sxs-lookup"><span data-stu-id="01fe8-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="01fe8-108">要查詢之介面的 **IDirect3DSurface9** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="01fe8-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="01fe8-109">*旗標*</span><span class="sxs-lookup"><span data-stu-id="01fe8-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="01fe8-110">指定要執行的查詢類型。</span><span class="sxs-lookup"><span data-stu-id="01fe8-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="01fe8-111">值</span><span class="sxs-lookup"><span data-stu-id="01fe8-111">Value</span></span>                                                                                                                             | <span data-ttu-id="01fe8-112">意義</span><span class="sxs-lookup"><span data-stu-id="01fe8-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="01fe8-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="01fe8-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="01fe8-114">測試介面是否可以安全地用於撰寫。</span><span class="sxs-lookup"><span data-stu-id="01fe8-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="01fe8-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="01fe8-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="01fe8-116">測試介面是否可安全用來進行讀取。</span><span class="sxs-lookup"><span data-stu-id="01fe8-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fe8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="01fe8-117">Return value</span></span>

<span data-ttu-id="01fe8-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="01fe8-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01fe8-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="01fe8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fe8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="01fe8-120">Requirements</span></span>



| <span data-ttu-id="01fe8-121">需求</span><span class="sxs-lookup"><span data-stu-id="01fe8-121">Requirement</span></span> | <span data-ttu-id="01fe8-122">值</span><span class="sxs-lookup"><span data-stu-id="01fe8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="01fe8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01fe8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="01fe8-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01fe8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01fe8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01fe8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="01fe8-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01fe8-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="01fe8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="01fe8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="01fe8-128"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="01fe8-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fe8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01fe8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fe8-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="01fe8-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




