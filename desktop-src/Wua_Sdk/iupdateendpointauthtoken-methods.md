---
description: IUpdateEndpointAuthToken 介面會定義下列方法。
ms.assetid: 955ED696-50C0-4E32-A5B7-C9E4E75836E3
title: IUpdateEndpointAuthToken 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9579bda43cc803835f38837a03a3b1c8bf4aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318503"
---
# <a name="iupdateendpointauthtoken-methods"></a><span data-ttu-id="abcce-103">IUpdateEndpointAuthToken 方法</span><span class="sxs-lookup"><span data-stu-id="abcce-103">IUpdateEndpointAuthToken Methods</span></span>

<span data-ttu-id="abcce-104">[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="abcce-104">The [**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md) interface defines the following methods.</span></span>



| <span data-ttu-id="abcce-105">方法</span><span class="sxs-lookup"><span data-stu-id="abcce-105">Method</span></span>                                                                                | <span data-ttu-id="abcce-106">描述</span><span class="sxs-lookup"><span data-stu-id="abcce-106">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abcce-107">**TokenData**</span><span class="sxs-lookup"><span data-stu-id="abcce-107">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="abcce-108">取得 XML 資料 (透過網路) 傳送，以代表權杖。</span><span class="sxs-lookup"><span data-stu-id="abcce-108">Gets the XML data (sent over the wire) that represents the token.</span></span>                                               |
| [<span data-ttu-id="abcce-109">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="abcce-109">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="abcce-110">取得端點 token 的型別，例如 WS-Security SAML (安全性聲明標記語言) 1.1 token。</span><span class="sxs-lookup"><span data-stu-id="abcce-110">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> |
| [<span data-ttu-id="abcce-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="abcce-111">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="abcce-112">取得要驗證之服務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="abcce-112">Gets the identifier of the service to be authenticated.</span></span>                                                         |
| [<span data-ttu-id="abcce-113">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="abcce-113">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="abcce-114">取得用來在用戶端電腦與 sercvice 之間簽署外寄訊息的金鑰。</span><span class="sxs-lookup"><span data-stu-id="abcce-114">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span>                       |
| [<span data-ttu-id="abcce-115">**TokenReferenceAttached**</span><span class="sxs-lookup"><span data-stu-id="abcce-115">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="abcce-116">取得 token 之附加參考的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="abcce-116">Gets the XML format of an attached reference to the token.</span></span>                                                      |
| [<span data-ttu-id="abcce-117">**TokenReferenceUnattached**</span><span class="sxs-lookup"><span data-stu-id="abcce-117">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="abcce-118">取得標記之未附加參考的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="abcce-118">Gets the XML format of an unattached reference to the token.</span></span>                                                    |



 

 

 



