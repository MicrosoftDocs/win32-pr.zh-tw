---
title: 'IEnumBackgroundCopyFiles Reset 方法 (>deliveryoptimization .h) '
description: 將列舉序列重設為開頭。
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset 方法
- Reset 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，Reset 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843384"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="fd5e0-106">IEnumBackgroundCopyFiles：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="fd5e0-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="fd5e0-107">將列舉序列重設為開頭。</span><span class="sxs-lookup"><span data-stu-id="fd5e0-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5e0-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd5e0-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="fd5e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="fd5e0-109">Parameters</span></span>

<span data-ttu-id="fd5e0-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fd5e0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd5e0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd5e0-111">Return value</span></span>

<span data-ttu-id="fd5e0-112">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fd5e0-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5e0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd5e0-113">Requirements</span></span>



| <span data-ttu-id="fd5e0-114">需求</span><span class="sxs-lookup"><span data-stu-id="fd5e0-114">Requirement</span></span> | <span data-ttu-id="fd5e0-115">值</span><span class="sxs-lookup"><span data-stu-id="fd5e0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5e0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd5e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5e0-117">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd5e0-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fd5e0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd5e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5e0-119">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd5e0-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fd5e0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fd5e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd5e0-121"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd5e0-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd5e0-122">Idl</span><span class="sxs-lookup"><span data-stu-id="fd5e0-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd5e0-123"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd5e0-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fd5e0-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd5e0-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd5e0-125"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd5e0-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fd5e0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fd5e0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd5e0-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd5e0-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fd5e0-128">IID</span><span class="sxs-lookup"><span data-stu-id="fd5e0-128">IID</span></span><br/>                      | <span data-ttu-id="fd5e0-129">IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="fd5e0-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="fd5e0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd5e0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5e0-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="fd5e0-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





