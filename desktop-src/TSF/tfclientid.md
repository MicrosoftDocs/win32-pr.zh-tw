---
title: 'TfClientId (Msctf) '
description: TfClientId 資料類型是用來識別用戶端。
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685751"
---
# <a name="tfclientid"></a><span data-ttu-id="255a7-104">TfClientId</span><span class="sxs-lookup"><span data-stu-id="255a7-104">TfClientId</span></span>

<span data-ttu-id="255a7-105">**TfClientId** 資料類型是用來識別用戶端。</span><span class="sxs-lookup"><span data-stu-id="255a7-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="255a7-106">備註</span><span class="sxs-lookup"><span data-stu-id="255a7-106">Remarks</span></span>

<span data-ttu-id="255a7-107">在 TSF 中，應用程式和文字服務通常稱為用戶端。</span><span class="sxs-lookup"><span data-stu-id="255a7-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="255a7-108">每個用戶端都會收到唯一的識別碼，以在呼叫各種 TSF manager 方法時用來識別其本身。</span><span class="sxs-lookup"><span data-stu-id="255a7-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="255a7-109">此識別碼屬於 **TfClientId** 類型。</span><span class="sxs-lookup"><span data-stu-id="255a7-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="255a7-110">**TfClientId** 資料類型是由 TSF 管理員所提供。</span><span class="sxs-lookup"><span data-stu-id="255a7-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="255a7-111">應用程式會在呼叫 [ITfThreadMgr：： Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)時取得 **TfClientId** 值。</span><span class="sxs-lookup"><span data-stu-id="255a7-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="255a7-112">文字服務的 TfClientId 值會傳遞至 [ITfTextInputProcessor：： Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) 方法。</span><span class="sxs-lookup"><span data-stu-id="255a7-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="255a7-113">任何不符合上述類別的物件都可以藉由呼叫 [ITfClientId：： GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)來取得用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="255a7-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="255a7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="255a7-114">Requirements</span></span>



| <span data-ttu-id="255a7-115">需求</span><span class="sxs-lookup"><span data-stu-id="255a7-115">Requirement</span></span> | <span data-ttu-id="255a7-116">值</span><span class="sxs-lookup"><span data-stu-id="255a7-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="255a7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="255a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="255a7-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="255a7-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="255a7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="255a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="255a7-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="255a7-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="255a7-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="255a7-121">Redistributable</span></span><br/>          | <span data-ttu-id="255a7-122">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="255a7-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="255a7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="255a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="255a7-124"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="255a7-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="255a7-125">Idl</span><span class="sxs-lookup"><span data-stu-id="255a7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="255a7-126"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="255a7-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="255a7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="255a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="255a7-128">**ITfClientId::GetClientId**</span><span class="sxs-lookup"><span data-stu-id="255a7-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="255a7-129">**ITfTextInputProcessor：： Activate**</span><span class="sxs-lookup"><span data-stu-id="255a7-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="255a7-130">**ITfThreadMgr：： Activate**</span><span class="sxs-lookup"><span data-stu-id="255a7-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





