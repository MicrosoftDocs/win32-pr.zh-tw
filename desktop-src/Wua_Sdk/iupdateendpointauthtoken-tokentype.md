---
description: 取得端點 token 的型別，例如 WS-Security SAML (安全性聲明標記語言) 1.1 token。
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'IUpdateEndpointAuthToken：： TokenType 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511780"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="dfcaf-103">IUpdateEndpointAuthToken：： TokenType 方法</span><span class="sxs-lookup"><span data-stu-id="dfcaf-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="dfcaf-104">取得端點 token 的型別，例如 WS-Security SAML (安全性聲明標記語言) 1.1 token。</span><span class="sxs-lookup"><span data-stu-id="dfcaf-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfcaf-105">語法</span><span class="sxs-lookup"><span data-stu-id="dfcaf-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="dfcaf-106">參數</span><span class="sxs-lookup"><span data-stu-id="dfcaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfcaf-107">*pTokenType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dfcaf-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcaf-108">端點 token 的型別。</span><span class="sxs-lookup"><span data-stu-id="dfcaf-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfcaf-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfcaf-109">Return value</span></span>

<span data-ttu-id="dfcaf-110">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="dfcaf-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="dfcaf-111">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dfcaf-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfcaf-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfcaf-112">Requirements</span></span>



| <span data-ttu-id="dfcaf-113">需求</span><span class="sxs-lookup"><span data-stu-id="dfcaf-113">Requirement</span></span> | <span data-ttu-id="dfcaf-114">值</span><span class="sxs-lookup"><span data-stu-id="dfcaf-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcaf-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfcaf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dfcaf-116">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfcaf-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="dfcaf-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfcaf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dfcaf-118">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="dfcaf-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="dfcaf-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dfcaf-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfcaf-120"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="dfcaf-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfcaf-121">Idl</span><span class="sxs-lookup"><span data-stu-id="dfcaf-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfcaf-122"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfcaf-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="dfcaf-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="dfcaf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfcaf-124"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfcaf-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="dfcaf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dfcaf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfcaf-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfcaf-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfcaf-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfcaf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfcaf-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="dfcaf-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




