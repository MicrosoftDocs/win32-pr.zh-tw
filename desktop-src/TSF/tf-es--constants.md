---
title: 'TF_ES_ 常數 (Msctf) '
description: 以下是 ITfCoNtext RequestEditSession 方法所使用的常數。
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995582"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="69875-103">TF \_ ES \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="69875-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="69875-104">以下是 [ITfCoNtext：： RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) 方法所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="69875-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="69875-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="69875-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="69875-106">Description</span><span class="sxs-lookup"><span data-stu-id="69875-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="69875-107"><dt>**TF \_ES \_ ASYNCDONTCARE**</dt> <dt> ( 0 )</dt></span><span class="sxs-lookup"><span data-stu-id="69875-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="69875-108">編輯會話可能會以同步或非同步方式進行，由管理員自行決定。</span><span class="sxs-lookup"><span data-stu-id="69875-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="69875-109">管理員會嘗試排程同步編輯會話，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="69875-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="69875-110">此值無法與 TF \_ es \_ ASYNC 或 tf \_ es \_ 同步值結合。</span><span class="sxs-lookup"><span data-stu-id="69875-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="69875-111"><dt>**TF \_ES \_ 同步**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="69875-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="69875-112">編輯會話必須是同步的，否則 (會有 TF \_ E 同步) 的要求將會失敗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="69875-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="69875-113">此旗標只能在記載的情況下使用 (例如按鍵處理，) 應該會成功。</span><span class="sxs-lookup"><span data-stu-id="69875-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="69875-114">否則呼叫可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="69875-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="69875-115">此值無法與 TF \_ es \_ ASYNCDONTCARE 或 tf \_ es \_ ASYNC 值結合。</span><span class="sxs-lookup"><span data-stu-id="69875-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="69875-116"><dt>**TF \_ES \_ READ**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="69875-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="69875-117">要求內容的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="69875-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="69875-118"><dt>**TF \_ES \_ READWRITE**</dt> <dt> ( 0x6 )</dt></span><span class="sxs-lookup"><span data-stu-id="69875-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="69875-119">要求內容的讀取/寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="69875-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="69875-120"><dt>**TF \_ES \_ ASYNC**</dt> <dt> ( 0x8 )</dt></span><span class="sxs-lookup"><span data-stu-id="69875-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="69875-121">編輯會話必須是非同步，否則要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="69875-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="69875-122">此值無法與 TF \_ es \_ ASYNCDONTCARE 或 tf \_ es \_ 同步值結合。</span><span class="sxs-lookup"><span data-stu-id="69875-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="69875-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="69875-123">Requirements</span></span>



| <span data-ttu-id="69875-124">需求</span><span class="sxs-lookup"><span data-stu-id="69875-124">Requirement</span></span> | <span data-ttu-id="69875-125">值</span><span class="sxs-lookup"><span data-stu-id="69875-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="69875-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69875-126">Minimum supported client</span></span><br/> | <span data-ttu-id="69875-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69875-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="69875-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69875-128">Minimum supported server</span></span><br/> | <span data-ttu-id="69875-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69875-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="69875-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="69875-130">Redistributable</span></span><br/>          | <span data-ttu-id="69875-131">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="69875-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="69875-132">標頭</span><span class="sxs-lookup"><span data-stu-id="69875-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="69875-133"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="69875-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="69875-134">Idl</span><span class="sxs-lookup"><span data-stu-id="69875-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69875-135"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="69875-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69875-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69875-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69875-137">ITfCoNtext：： RequestEditSession</span><span class="sxs-lookup"><span data-stu-id="69875-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





