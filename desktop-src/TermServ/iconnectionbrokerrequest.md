---
title: 'IConnectionBrokerRequest 介面 (Cbclient .h) '
description: 提供取得非同步 IConnectionBrokerClient GetTargetInfo 方法之結果所需的方法。
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- IConnectionBrokerRequest 介面遠端桌面服務
- IConnectionBrokerRequest 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686508"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="68abe-105">IConnectionBrokerRequest 介面</span><span class="sxs-lookup"><span data-stu-id="68abe-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="68abe-106">提供取得非同步 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法之結果所需的方法。</span><span class="sxs-lookup"><span data-stu-id="68abe-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="68abe-107">此介面是由系統所執行。</span><span class="sxs-lookup"><span data-stu-id="68abe-107">This interface is implemented by the system.</span></span> <span data-ttu-id="68abe-108">使用 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法，將這個介面的實例提供給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="68abe-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="68abe-109">成員</span><span class="sxs-lookup"><span data-stu-id="68abe-109">Members</span></span>

<span data-ttu-id="68abe-110">**IConnectionBrokerRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="68abe-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="68abe-111">**IConnectionBrokerRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="68abe-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="68abe-112">方法</span><span class="sxs-lookup"><span data-stu-id="68abe-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68abe-113">方法</span><span class="sxs-lookup"><span data-stu-id="68abe-113">Methods</span></span>

<span data-ttu-id="68abe-114">**IConnectionBrokerRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="68abe-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="68abe-115">方法</span><span class="sxs-lookup"><span data-stu-id="68abe-115">Method</span></span>                                                      | <span data-ttu-id="68abe-116">描述</span><span class="sxs-lookup"><span data-stu-id="68abe-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="68abe-117">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="68abe-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="68abe-118">呼叫以判斷非同步要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="68abe-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="68abe-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="68abe-119">Requirements</span></span>



| <span data-ttu-id="68abe-120">需求</span><span class="sxs-lookup"><span data-stu-id="68abe-120">Requirement</span></span> | <span data-ttu-id="68abe-121">值</span><span class="sxs-lookup"><span data-stu-id="68abe-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="68abe-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68abe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68abe-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68abe-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="68abe-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68abe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68abe-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68abe-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="68abe-126">標頭</span><span class="sxs-lookup"><span data-stu-id="68abe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68abe-127"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="68abe-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="68abe-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="68abe-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="68abe-129"><dt>Cbclient .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68abe-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="68abe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="68abe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68abe-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68abe-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="68abe-132">IID</span><span class="sxs-lookup"><span data-stu-id="68abe-132">IID</span></span><br/>                      | <span data-ttu-id="68abe-133">IID \_ IConnectionBrokerRequest 定義為 25114427-ED5D-46A6-AF53-C62D33A4108E</span><span class="sxs-lookup"><span data-stu-id="68abe-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68abe-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68abe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68abe-135">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="68abe-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

