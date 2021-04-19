---
title: 安全性處理結果
description: 在安全通道上，只有成功通過安全性檢查的訊息會傳遞至應用程式。
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- 適用于 Windows 的安全性處理結果 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106969947"
---
# <a name="security-processing-results"></a><span data-ttu-id="ae484-106">安全性處理結果</span><span class="sxs-lookup"><span data-stu-id="ae484-106">Security Processing Results</span></span>

<span data-ttu-id="ae484-107">在安全通道上，只有成功通過安全性檢查的訊息會傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="ae484-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="ae484-108">針對這些訊息，安全性驗證的一些結果會以訊息屬性的形式附加，而應用程式可能會解壓縮並檢查這些屬性，以執行其他步驟，例如授權檢查。</span><span class="sxs-lookup"><span data-stu-id="ae484-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="ae484-109">函數 [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) 可用來取出 [**WS \_ MESSAGE \_ PROPERTY \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)中定義的任何安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="ae484-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="ae484-110">如果查詢要求的安全性屬性不適用於通道上使用的安全性類型， **WsGetMessageProperty** 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ae484-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="ae484-111">訊息會繼續擁有查詢函數所傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae484-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="ae484-112">下列 API 元素用於安全性處理結果。</span><span class="sxs-lookup"><span data-stu-id="ae484-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="ae484-113">列舉型別</span><span class="sxs-lookup"><span data-stu-id="ae484-113">Enumeration</span></span>                                                                | <span data-ttu-id="ae484-114">描述</span><span class="sxs-lookup"><span data-stu-id="ae484-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae484-115">**WS \_ 安全性 \_ 權杖 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="ae484-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="ae484-116">定義可以從安全性權杖解壓縮之欄位和屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ae484-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="ae484-117">函式</span><span class="sxs-lookup"><span data-stu-id="ae484-117">Function</span></span>                                                         | <span data-ttu-id="ae484-118">描述</span><span class="sxs-lookup"><span data-stu-id="ae484-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="ae484-119">**WsGetSecurityTokenProperty**</span><span class="sxs-lookup"><span data-stu-id="ae484-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="ae484-120">從安全性權杖中解壓縮欄位或屬性。</span><span class="sxs-lookup"><span data-stu-id="ae484-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="ae484-121">Handle</span><span class="sxs-lookup"><span data-stu-id="ae484-121">Handle</span></span>                                       | <span data-ttu-id="ae484-122">Description</span><span class="sxs-lookup"><span data-stu-id="ae484-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ae484-123">WS \_ 安全性 \_ 權杖</span><span class="sxs-lookup"><span data-stu-id="ae484-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="ae484-124">代表安全性權杖的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="ae484-124">An opaque handle representing a security token.</span></span> |



 

 

 




