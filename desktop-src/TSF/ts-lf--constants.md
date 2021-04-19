---
title: 'TS_LF_ 常數 (Textstor) '
description: TS \_ LF \_ \ 常數會指定檔鎖定的類型。
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969133"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="07be7-103">TS \_ LF \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="07be7-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="07be7-104">TS \_ LF \_ \* 常數會指定檔鎖定的類型。</span><span class="sxs-lookup"><span data-stu-id="07be7-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="07be7-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="07be7-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="07be7-106">Description</span><span class="sxs-lookup"><span data-stu-id="07be7-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="07be7-107"><dt>**TS \_LF \_ 同步**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="07be7-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="07be7-108">如果此旗標與其他旗標合併，則檔具有同步鎖定。</span><span class="sxs-lookup"><span data-stu-id="07be7-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="07be7-109"><dt>**TS \_LF \_ READ**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="07be7-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="07be7-110">檔有唯讀鎖定，無法修改。</span><span class="sxs-lookup"><span data-stu-id="07be7-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="07be7-111"><dt>**TS \_LF \_ READWRITE**</dt> <dt> ( 0x6 )</dt></span><span class="sxs-lookup"><span data-stu-id="07be7-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="07be7-112">檔具有讀取/寫入鎖定，而且可以修改。</span><span class="sxs-lookup"><span data-stu-id="07be7-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="07be7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="07be7-113">Requirements</span></span>



| <span data-ttu-id="07be7-114">需求</span><span class="sxs-lookup"><span data-stu-id="07be7-114">Requirement</span></span> | <span data-ttu-id="07be7-115">值</span><span class="sxs-lookup"><span data-stu-id="07be7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07be7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07be7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07be7-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07be7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="07be7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07be7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07be7-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07be7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07be7-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="07be7-120">Redistributable</span></span><br/>          | <span data-ttu-id="07be7-121">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="07be7-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="07be7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="07be7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07be7-123"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="07be7-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="07be7-124">Idl</span><span class="sxs-lookup"><span data-stu-id="07be7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07be7-125"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="07be7-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07be7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07be7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07be7-127">檔鎖定</span><span class="sxs-lookup"><span data-stu-id="07be7-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="07be7-128">ITextStoreACP：： RequestLock</span><span class="sxs-lookup"><span data-stu-id="07be7-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="07be7-129">ITextStoreACPSink：： OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="07be7-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="07be7-130">ITextStoreAnchor：： RequestLock</span><span class="sxs-lookup"><span data-stu-id="07be7-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="07be7-131">ITextStoreAnchorSink：： OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="07be7-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





