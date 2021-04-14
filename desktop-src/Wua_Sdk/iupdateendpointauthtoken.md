---
description: 提供 WUA 可用來收集端點 token 相關資訊的方法。
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: 'IUpdateEndpointAuthToken 介面 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469156"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="9f8cb-103">IUpdateEndpointAuthToken 介面</span><span class="sxs-lookup"><span data-stu-id="9f8cb-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="9f8cb-104">提供 WUA 可用來收集端點 token 相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="9f8cb-105">成員</span><span class="sxs-lookup"><span data-stu-id="9f8cb-105">Members</span></span>

<span data-ttu-id="9f8cb-106">**IUpdateEndpointAuthToken** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9f8cb-107">**IUpdateEndpointAuthToken** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9f8cb-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="9f8cb-108">方法</span><span class="sxs-lookup"><span data-stu-id="9f8cb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9f8cb-109">方法</span><span class="sxs-lookup"><span data-stu-id="9f8cb-109">Methods</span></span>

<span data-ttu-id="9f8cb-110">**IUpdateEndpointAuthToken** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="9f8cb-111">方法</span><span class="sxs-lookup"><span data-stu-id="9f8cb-111">Method</span></span>                                                                                | <span data-ttu-id="9f8cb-112">描述</span><span class="sxs-lookup"><span data-stu-id="9f8cb-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f8cb-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="9f8cb-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="9f8cb-114">取得要驗證之服務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="9f8cb-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="9f8cb-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="9f8cb-116">取得用來在用戶端電腦與 sercvice 之間簽署外寄訊息的金鑰。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="9f8cb-117">**TokenData**</span><span class="sxs-lookup"><span data-stu-id="9f8cb-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="9f8cb-118">取得 XML 資料 (透過網路) 傳送，以代表權杖。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="9f8cb-119">**TokenReferenceAttached**</span><span class="sxs-lookup"><span data-stu-id="9f8cb-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="9f8cb-120">取得 token 之附加參考的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="9f8cb-121">**TokenReferenceUnattached**</span><span class="sxs-lookup"><span data-stu-id="9f8cb-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="9f8cb-122">取得標記之未附加參考的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="9f8cb-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="9f8cb-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="9f8cb-124">取得端點 token 的型別，例如 WS-Security SAML (安全性聲明標記語言) 1.1 token。</span><span class="sxs-lookup"><span data-stu-id="9f8cb-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="9f8cb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f8cb-125">Requirements</span></span>



| <span data-ttu-id="9f8cb-126">需求</span><span class="sxs-lookup"><span data-stu-id="9f8cb-126">Requirement</span></span> | <span data-ttu-id="9f8cb-127">值</span><span class="sxs-lookup"><span data-stu-id="9f8cb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8cb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f8cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f8cb-129">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f8cb-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="9f8cb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f8cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f8cb-131">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="9f8cb-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="9f8cb-132">標頭</span><span class="sxs-lookup"><span data-stu-id="9f8cb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f8cb-133"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f8cb-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f8cb-134">Idl</span><span class="sxs-lookup"><span data-stu-id="9f8cb-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f8cb-135"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f8cb-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f8cb-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f8cb-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f8cb-137"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f8cb-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f8cb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8cb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f8cb-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8cb-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
