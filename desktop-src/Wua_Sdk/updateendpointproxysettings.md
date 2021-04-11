---
description: UpdateEndpointProxySettings 結構會定義要求權杖時所使用的 proxy 設定。
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: 'UpdateEndpointProxySettings 結構 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026269"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="e562b-103">UpdateEndpointProxySettings 結構</span><span class="sxs-lookup"><span data-stu-id="e562b-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="e562b-104">**UpdateEndpointProxySettings** 結構會定義要求權杖時所使用的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="e562b-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="e562b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e562b-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="e562b-106">成員</span><span class="sxs-lookup"><span data-stu-id="e562b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e562b-107">**szProxyAddr**</span><span class="sxs-lookup"><span data-stu-id="e562b-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="e562b-108">要使用 (proxy 伺服器的 DNS 名稱或 IP 位址，例如 "proxy.somecorp.com" 或 "192.168.0.4" ) ，如果未使用 proxy，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="e562b-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e562b-109">**szBypassList**</span><span class="sxs-lookup"><span data-stu-id="e562b-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="e562b-110">應略過 proxy 伺服器的主機位址清單; 如果所有主機位址都應該使用 proxy 伺服器，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="e562b-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="e562b-111">如果 **szProxyAddr** 是空的，則 WUA 不會使用此資料。</span><span class="sxs-lookup"><span data-stu-id="e562b-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="e562b-112">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="e562b-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="e562b-113">用來向 proxy 伺服器進行驗證的使用者名稱，如果不需要驗證，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="e562b-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="e562b-114">如果 **szProxyAddr** 是空的，則 WUA 不會使用此資料。</span><span class="sxs-lookup"><span data-stu-id="e562b-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="e562b-115">**szPassword**</span><span class="sxs-lookup"><span data-stu-id="e562b-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="e562b-116">用來向 proxy 伺服器進行驗證的密碼，如果不需要驗證，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="e562b-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="e562b-117">如果 **szProxyAddr** 是空的，則 WUA 不會使用此資料。</span><span class="sxs-lookup"><span data-stu-id="e562b-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e562b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e562b-118">Requirements</span></span>



| <span data-ttu-id="e562b-119">需求</span><span class="sxs-lookup"><span data-stu-id="e562b-119">Requirement</span></span> | <span data-ttu-id="e562b-120">值</span><span class="sxs-lookup"><span data-stu-id="e562b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e562b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e562b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e562b-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e562b-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="e562b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e562b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e562b-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e562b-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e562b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e562b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e562b-126"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="e562b-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="e562b-127">Idl</span><span class="sxs-lookup"><span data-stu-id="e562b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e562b-128"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e562b-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e562b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e562b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e562b-130">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="e562b-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




