---
title: 'IConnectionBrokerClient 介面 (Cbclient .h) '
description: 提供使用遠端桌面連線代理人用戶端所需的方法。
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- IConnectionBrokerClient 介面遠端桌面服務
- IConnectionBrokerClient 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466757"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="1774e-105">IConnectionBrokerClient 介面</span><span class="sxs-lookup"><span data-stu-id="1774e-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="1774e-106">提供使用遠端桌面連線代理人用戶端所需的方法。</span><span class="sxs-lookup"><span data-stu-id="1774e-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="1774e-107">此介面是由系統所執行。</span><span class="sxs-lookup"><span data-stu-id="1774e-107">This interface is implemented by the system.</span></span> <span data-ttu-id="1774e-108">若要取得這個介面的實例，請使用 [**CBCreateClientInstance**](cbcreateclientinstance.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="1774e-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="1774e-109">成員</span><span class="sxs-lookup"><span data-stu-id="1774e-109">Members</span></span>

<span data-ttu-id="1774e-110">**IConnectionBrokerClient** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1774e-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1774e-111">**IConnectionBrokerClient** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1774e-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="1774e-112">方法</span><span class="sxs-lookup"><span data-stu-id="1774e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1774e-113">方法</span><span class="sxs-lookup"><span data-stu-id="1774e-113">Methods</span></span>

<span data-ttu-id="1774e-114">**IConnectionBrokerClient** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1774e-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="1774e-115">方法</span><span class="sxs-lookup"><span data-stu-id="1774e-115">Method</span></span>                                                         | <span data-ttu-id="1774e-116">描述</span><span class="sxs-lookup"><span data-stu-id="1774e-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1774e-117">**GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="1774e-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="1774e-118">要求應重新導向連接之目的電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1774e-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1774e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1774e-119">Requirements</span></span>



| <span data-ttu-id="1774e-120">需求</span><span class="sxs-lookup"><span data-stu-id="1774e-120">Requirement</span></span> | <span data-ttu-id="1774e-121">值</span><span class="sxs-lookup"><span data-stu-id="1774e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1774e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1774e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1774e-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1774e-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="1774e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1774e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1774e-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1774e-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="1774e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="1774e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1774e-127"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="1774e-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="1774e-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="1774e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="1774e-129"><dt>Cbclient .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1774e-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="1774e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1774e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1774e-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1774e-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="1774e-132">IID</span><span class="sxs-lookup"><span data-stu-id="1774e-132">IID</span></span><br/>                      | <span data-ttu-id="1774e-133">IID \_ IConnectionBrokerClient 定義為 D6818DF2-8338-4EB7-AD77-DE210817987C</span><span class="sxs-lookup"><span data-stu-id="1774e-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1774e-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1774e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1774e-135">**CBCreateClientInstance**</span><span class="sxs-lookup"><span data-stu-id="1774e-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 

