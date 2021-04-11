---
title: 'TF_SD_ 常數 (Msctf) '
description: TF \_ SD \_ \ 常數描述檔狀態。
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093963"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="9cfaf-103">TF \_ SD \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="9cfaf-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="9cfaf-104">TF \_ SD \_ \* 常數描述檔狀態。</span><span class="sxs-lookup"><span data-stu-id="9cfaf-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="9cfaf-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="9cfaf-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="9cfaf-106">Description</span><span class="sxs-lookup"><span data-stu-id="9cfaf-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="9cfaf-107"><dt>**TF \_SD \_ readonly**</dt> <dt> ( TS \_ SD \_ readonly )</dt></span><span class="sxs-lookup"><span data-stu-id="9cfaf-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="9cfaf-108">檔是唯讀的，而且無法修改。</span><span class="sxs-lookup"><span data-stu-id="9cfaf-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="9cfaf-109"><dt>**TF \_\_**</dt> <dt> ( TS \_ SD \_ 載入 )</dt>的 SD 載入</span><span class="sxs-lookup"><span data-stu-id="9cfaf-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="9cfaf-110">檔正在載入，而且可能不完整。</span><span class="sxs-lookup"><span data-stu-id="9cfaf-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="9cfaf-111">備註</span><span class="sxs-lookup"><span data-stu-id="9cfaf-111">Remarks</span></span>

<span data-ttu-id="9cfaf-112">[TF \_ 狀態](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))結構的 **dwDynamicFlags** 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="9cfaf-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cfaf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cfaf-113">Requirements</span></span>



| <span data-ttu-id="9cfaf-114">需求</span><span class="sxs-lookup"><span data-stu-id="9cfaf-114">Requirement</span></span> | <span data-ttu-id="9cfaf-115">值</span><span class="sxs-lookup"><span data-stu-id="9cfaf-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfaf-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9cfaf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9cfaf-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9cfaf-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9cfaf-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9cfaf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9cfaf-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9cfaf-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9cfaf-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9cfaf-120">Redistributable</span></span><br/>          | <span data-ttu-id="9cfaf-121">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="9cfaf-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="9cfaf-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9cfaf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cfaf-123"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="9cfaf-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cfaf-124">Idl</span><span class="sxs-lookup"><span data-stu-id="9cfaf-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9cfaf-125"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9cfaf-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cfaf-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cfaf-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9cfaf-127">[TF \_ 狀態](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfaf-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9cfaf-128">TS \_ SD \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="9cfaf-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="9cfaf-129">ITfCoNtextOwner：： GetStatus</span><span class="sxs-lookup"><span data-stu-id="9cfaf-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="9cfaf-130">ITfCoNtextOwnerServices::OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="9cfaf-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="9cfaf-131">ITextStoreACP：： GetStatus</span><span class="sxs-lookup"><span data-stu-id="9cfaf-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="9cfaf-132">ITfStatusSunk::OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="9cfaf-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

