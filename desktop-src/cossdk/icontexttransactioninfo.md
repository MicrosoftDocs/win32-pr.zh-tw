---
description: 提供與交易相關之內容物件屬性的存取權。
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: ICoNtextTransactionInfo 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468305"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="2e359-103">ICoNtextTransactionInfo 介面</span><span class="sxs-lookup"><span data-stu-id="2e359-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="2e359-104">提供與交易相關之內容物件屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="2e359-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2e359-105">執行時機</span><span class="sxs-lookup"><span data-stu-id="2e359-105">When to implement</span></span>

<span data-ttu-id="2e359-106">您不應該執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="2e359-106">You should not implement this interface.</span></span> <span data-ttu-id="2e359-107">標準實作為提供完整的功能。</span><span class="sxs-lookup"><span data-stu-id="2e359-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2e359-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="2e359-108">When to use</span></span>

<span data-ttu-id="2e359-109">您可以使用這個介面來存取與交易相關的內容物件屬性。</span><span class="sxs-lookup"><span data-stu-id="2e359-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="2e359-110">成員</span><span class="sxs-lookup"><span data-stu-id="2e359-110">Members</span></span>

<span data-ttu-id="2e359-111">**ICoNtextTransactionInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2e359-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e359-112">**ICoNtextTransactionInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2e359-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="2e359-113">方法</span><span class="sxs-lookup"><span data-stu-id="2e359-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e359-114">方法</span><span class="sxs-lookup"><span data-stu-id="2e359-114">Methods</span></span>

<span data-ttu-id="2e359-115">**ICoNtextTransactionInfo** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2e359-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="2e359-116">方法</span><span class="sxs-lookup"><span data-stu-id="2e359-116">Method</span></span>                                                                                         | <span data-ttu-id="2e359-117">描述</span><span class="sxs-lookup"><span data-stu-id="2e359-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e359-118">**FetchTransaction**</span><span class="sxs-lookup"><span data-stu-id="2e359-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="2e359-119">抓取與目前內容相關聯的交易或交易 proxy （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2e359-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="2e359-120">**GetTxIsolationLevelAndTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e359-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="2e359-121">抓取根交易內容中所裝載之交易的隔離等級和超時值。</span><span class="sxs-lookup"><span data-stu-id="2e359-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="2e359-122">**RegisterTransactionProxy**</span><span class="sxs-lookup"><span data-stu-id="2e359-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="2e359-123">將 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 的執行與目前的內容產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2e359-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="2e359-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e359-124">Requirements</span></span>



| <span data-ttu-id="2e359-125">需求</span><span class="sxs-lookup"><span data-stu-id="2e359-125">Requirement</span></span> | <span data-ttu-id="2e359-126">值</span><span class="sxs-lookup"><span data-stu-id="2e359-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2e359-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e359-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e359-128">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e359-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2e359-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e359-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e359-130">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e359-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 

