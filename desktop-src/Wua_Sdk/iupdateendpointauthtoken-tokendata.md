---
description: 取得 XML 資料 (透過網路) 傳送，以代表權杖。
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'IUpdateEndpointAuthToken：： TokenData 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970198"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="3ef84-103">IUpdateEndpointAuthToken：： TokenData 方法</span><span class="sxs-lookup"><span data-stu-id="3ef84-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="3ef84-104">取得 XML 資料 (透過網路) 傳送，以代表權杖。</span><span class="sxs-lookup"><span data-stu-id="3ef84-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef84-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ef84-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="3ef84-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ef84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ef84-107">*pszTokenData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ef84-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef84-108">XML 資料 (透過代表權杖的網路) 傳送。</span><span class="sxs-lookup"><span data-stu-id="3ef84-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="3ef84-109">例如，WS-Security SAML (安全性聲明標記語言) 1.1 token 的資料是新增至要求的 SAML 程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ef84-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ef84-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ef84-110">Return value</span></span>

<span data-ttu-id="3ef84-111">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="3ef84-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="3ef84-112">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3ef84-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef84-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ef84-113">Requirements</span></span>



| <span data-ttu-id="3ef84-114">需求</span><span class="sxs-lookup"><span data-stu-id="3ef84-114">Requirement</span></span> | <span data-ttu-id="3ef84-115">值</span><span class="sxs-lookup"><span data-stu-id="3ef84-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef84-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ef84-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef84-117">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ef84-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="3ef84-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ef84-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef84-119">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="3ef84-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="3ef84-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3ef84-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ef84-121"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef84-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ef84-122">Idl</span><span class="sxs-lookup"><span data-stu-id="3ef84-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ef84-123"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ef84-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ef84-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ef84-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ef84-125"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ef84-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ef84-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3ef84-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ef84-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ef84-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef84-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ef84-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef84-129">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="3ef84-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




