---
description: 包含用來取得用於連接服務之端點的方法。
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: IUpdateEndpointProvider 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972240"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="7c533-103">IUpdateEndpointProvider 介面</span><span class="sxs-lookup"><span data-stu-id="7c533-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="7c533-104">包含用來取得用於連接服務之端點的方法。</span><span class="sxs-lookup"><span data-stu-id="7c533-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="7c533-105">此介面會在撰寫端點提供者時執行。</span><span class="sxs-lookup"><span data-stu-id="7c533-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="7c533-106">成員</span><span class="sxs-lookup"><span data-stu-id="7c533-106">Members</span></span>

<span data-ttu-id="7c533-107">**IUpdateEndpointProvider** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7c533-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7c533-108">**IUpdateEndpointProvider** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7c533-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="7c533-109">方法</span><span class="sxs-lookup"><span data-stu-id="7c533-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c533-110">方法</span><span class="sxs-lookup"><span data-stu-id="7c533-110">Methods</span></span>

<span data-ttu-id="7c533-111">**IUpdateEndpointProvider** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7c533-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="7c533-112">方法</span><span class="sxs-lookup"><span data-stu-id="7c533-112">Method</span></span>                                                                       | <span data-ttu-id="7c533-113">描述</span><span class="sxs-lookup"><span data-stu-id="7c533-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="7c533-114">**GetServiceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="7c533-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="7c533-115">要求用來連接到服務的端點。</span><span class="sxs-lookup"><span data-stu-id="7c533-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c533-116">備註</span><span class="sxs-lookup"><span data-stu-id="7c533-116">Remarks</span></span>

<span data-ttu-id="7c533-117">WUA 會呼叫 [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) 方法來啟動協調進程。</span><span class="sxs-lookup"><span data-stu-id="7c533-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="7c533-118">進行呼叫時，WUA 會傳入已註冊的權杖類型，而此介面的執行會傳回它慣用使用的權杖類型。</span><span class="sxs-lookup"><span data-stu-id="7c533-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
