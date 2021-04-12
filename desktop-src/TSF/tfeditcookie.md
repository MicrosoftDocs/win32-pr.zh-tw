---
title: 'TfEditCookie (Msctf) '
description: TfEditCookie 資料類型會識別具有鎖定的編輯會話。
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024548"
---
# <a name="tfeditcookie"></a><span data-ttu-id="c5c8e-104">TfEditCookie</span><span class="sxs-lookup"><span data-stu-id="c5c8e-104">TfEditCookie</span></span>

<span data-ttu-id="c5c8e-105">**TfEditCookie** 資料類型會識別具有鎖定的編輯會話。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="c5c8e-106">備註</span><span class="sxs-lookup"><span data-stu-id="c5c8e-106">Remarks</span></span>

<span data-ttu-id="c5c8e-107">**TfEditCookie** 資料類型是由 TSF 管理員提供，而且用戶端 (應用程式或文字服務) 用來識別各種方法中具有唯讀或讀取/寫入鎖定的編輯會話。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="c5c8e-108">**TfEditCookie** 值是以下列其中一種方式取得。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="c5c8e-109">用戶端會呼叫 [ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="c5c8e-110">TSF 管理員會呼叫用戶端 [ITfEditSession：:D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="c5c8e-111">TSF 管理員會呼叫 client [ITfCompositionSink：： OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="c5c8e-112">TSF 管理員會呼叫 client [ITfCleanupCoNtextSink：： OnCleanupCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="c5c8e-113">TSF 管理員會呼叫 client [ITfTextEditSink：： OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5c8e-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c8e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5c8e-114">Requirements</span></span>



| <span data-ttu-id="c5c8e-115">需求</span><span class="sxs-lookup"><span data-stu-id="c5c8e-115">Requirement</span></span> | <span data-ttu-id="c5c8e-116">值</span><span class="sxs-lookup"><span data-stu-id="c5c8e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c8e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5c8e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c8e-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5c8e-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="c5c8e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5c8e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c8e-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5c8e-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c5c8e-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c5c8e-121">Redistributable</span></span><br/>          | <span data-ttu-id="c5c8e-122">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="c5c8e-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="c5c8e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c5c8e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c8e-124"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c8e-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5c8e-125">Idl</span><span class="sxs-lookup"><span data-stu-id="c5c8e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5c8e-126"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5c8e-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c8e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5c8e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c8e-128">**ITfCleanupCoNtextSink::OnCleanupCoNtext**</span><span class="sxs-lookup"><span data-stu-id="c5c8e-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="c5c8e-129">**ITfCompositionSink::OnCompositionTerminated**</span><span class="sxs-lookup"><span data-stu-id="c5c8e-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="c5c8e-130">**ITfDocumentMgr：： CreateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="c5c8e-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="c5c8e-131">**ITfEditSession：:D oEditSession**</span><span class="sxs-lookup"><span data-stu-id="c5c8e-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="c5c8e-132">**ITfTextEditSink::OnEndEdit**</span><span class="sxs-lookup"><span data-stu-id="c5c8e-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





