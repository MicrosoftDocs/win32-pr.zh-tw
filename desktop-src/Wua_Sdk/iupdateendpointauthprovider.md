---
description: 包含用來協商用來驗證服務端點的權杖類型的方法。
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: 'IUpdateEndpointAuthProvider 介面 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511784"
---
# <a name="iupdateendpointauthprovider-interface"></a><span data-ttu-id="f7490-103">IUpdateEndpointAuthProvider 介面</span><span class="sxs-lookup"><span data-stu-id="f7490-103">IUpdateEndpointAuthProvider interface</span></span>

<span data-ttu-id="f7490-104">**IUpdateEndpointAuthProvider** 介面包含用來協商用來驗證服務端點的權杖類型的方法。</span><span class="sxs-lookup"><span data-stu-id="f7490-104">The **IUpdateEndpointAuthProvider** interface contains the methods used for negotiating which type of token is used for authenticating the endpoint of a service.</span></span>

## <a name="members"></a><span data-ttu-id="f7490-105">成員</span><span class="sxs-lookup"><span data-stu-id="f7490-105">Members</span></span>

<span data-ttu-id="f7490-106">**IUpdateEndpointAuthProvider** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f7490-106">The **IUpdateEndpointAuthProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f7490-107">**IUpdateEndpointAuthProvider** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f7490-107">**IUpdateEndpointAuthProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="f7490-108">方法</span><span class="sxs-lookup"><span data-stu-id="f7490-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7490-109">方法</span><span class="sxs-lookup"><span data-stu-id="f7490-109">Methods</span></span>

<span data-ttu-id="f7490-110">**IUpdateEndpointAuthProvider** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f7490-110">The **IUpdateEndpointAuthProvider** interface has these methods.</span></span>



| <span data-ttu-id="f7490-111">方法</span><span class="sxs-lookup"><span data-stu-id="f7490-111">Method</span></span>                                                                                             | <span data-ttu-id="f7490-112">描述</span><span class="sxs-lookup"><span data-stu-id="f7490-112">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7490-113">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="f7490-113">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)                           | <span data-ttu-id="f7490-114">使用指定的認證，要求服務端點的權杖。</span><span class="sxs-lookup"><span data-stu-id="f7490-114">Request a token for the endpoint of the service using the specified credentials.</span></span><br/>    |
| [<span data-ttu-id="f7490-115">**GetPreferredEndpointTokenType**</span><span class="sxs-lookup"><span data-stu-id="f7490-115">**GetPreferredEndpointTokenType**</span></span>](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | <span data-ttu-id="f7490-116">傳回服務端點的慣用驗證 token 類型。</span><span class="sxs-lookup"><span data-stu-id="f7490-116">Returns the preferred type of authentication token for the endpoint of the service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7490-117">備註</span><span class="sxs-lookup"><span data-stu-id="f7490-117">Remarks</span></span>

<span data-ttu-id="f7490-118">WUA 會呼叫這個介面的 [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) 方法，以啟動協調進程。</span><span class="sxs-lookup"><span data-stu-id="f7490-118">WUA calls the [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) method of this interface to start the negotiation process.</span></span> <span data-ttu-id="f7490-119">當進行呼叫時，會將服務識別碼、服務所執行的端點類型，以及可用的權杖類型傳遞給 WUA。</span><span class="sxs-lookup"><span data-stu-id="f7490-119">When the call is made WUA passes in the service identifier, the type of endpoint implemented by the service, and the token types that are available.</span></span> <span data-ttu-id="f7490-120">然後，此介面的執行會傳回它所 preferes 要使用的權杖類型。</span><span class="sxs-lookup"><span data-stu-id="f7490-120">The implementation of this interface then returns the token types that it preferes to use.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7490-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7490-121">Requirements</span></span>



| <span data-ttu-id="f7490-122">需求</span><span class="sxs-lookup"><span data-stu-id="f7490-122">Requirement</span></span> | <span data-ttu-id="f7490-123">值</span><span class="sxs-lookup"><span data-stu-id="f7490-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7490-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7490-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7490-125">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7490-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="f7490-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7490-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7490-127">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="f7490-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f7490-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f7490-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7490-129"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7490-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7490-130">Idl</span><span class="sxs-lookup"><span data-stu-id="f7490-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7490-131"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7490-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7490-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7490-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7490-133"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7490-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7490-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f7490-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7490-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7490-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
