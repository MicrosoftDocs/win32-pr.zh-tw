---
description: 定義可用來向端點驗證的標記類型。
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: 'UpdateEndpointAuthTokenType 列舉 (UpdateEndpointAuth) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984161"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="2bf6c-103">UpdateEndpointAuthTokenType 列舉</span><span class="sxs-lookup"><span data-stu-id="2bf6c-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="2bf6c-104">定義可用來向端點驗證的標記類型。</span><span class="sxs-lookup"><span data-stu-id="2bf6c-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bf6c-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="2bf6c-106">常數</span><span class="sxs-lookup"><span data-stu-id="2bf6c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2bf6c-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span><span class="sxs-lookup"><span data-stu-id="2bf6c-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="2bf6c-108">不需要驗證權杖。</span><span class="sxs-lookup"><span data-stu-id="2bf6c-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="2bf6c-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="2bf6c-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="2bf6c-110">端點的驗證權杖是 WS-Security 的 SAML (安全性聲明標記語言) 1.1 權杖。</span><span class="sxs-lookup"><span data-stu-id="2bf6c-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bf6c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bf6c-111">Requirements</span></span>



| <span data-ttu-id="2bf6c-112">需求</span><span class="sxs-lookup"><span data-stu-id="2bf6c-112">Requirement</span></span> | <span data-ttu-id="2bf6c-113">值</span><span class="sxs-lookup"><span data-stu-id="2bf6c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf6c-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bf6c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2bf6c-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bf6c-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="2bf6c-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bf6c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2bf6c-117">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bf6c-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2bf6c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2bf6c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bf6c-119"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bf6c-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bf6c-120">Idl</span><span class="sxs-lookup"><span data-stu-id="2bf6c-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bf6c-121"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bf6c-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




