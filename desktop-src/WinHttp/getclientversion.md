---
description: 取得 WPAD 處理引擎的版本。
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850115"
---
# <a name="getclientversion-function"></a><span data-ttu-id="a7ef8-103">getClientVersion 函式</span><span class="sxs-lookup"><span data-stu-id="a7ef8-103">getClientVersion function</span></span>

<span data-ttu-id="a7ef8-104">取得 WPAD 處理引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7ef8-105">參數</span><span class="sxs-lookup"><span data-stu-id="a7ef8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ef8-106">*IpAddressList*</span><span class="sxs-lookup"><span data-stu-id="a7ef8-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="a7ef8-107">以分號分隔的字串，其中包含 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ef8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7ef8-108">Return value</span></span>

<span data-ttu-id="a7ef8-109">已排序之分號分隔 IP 位址的清單，如果無法排序 IP 位址清單，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7ef8-110">備註</span><span class="sxs-lookup"><span data-stu-id="a7ef8-110">Remarks</span></span>

<span data-ttu-id="a7ef8-111">此函數目前會傳回1.0 版。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="a7ef8-112">Microsoft 新增了此函式，可讓 IT 系統管理員將其 WPAD 腳本更新為使用不同版本的 WPAD 處理引擎，而不會導致中斷現有的部署。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="a7ef8-113">例如，如果 Microsoft 將函式新增至2.0 版的 WPAD 引擎，則系統管理員可以在嘗試呼叫該函式之前，先檢查版本。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="a7ef8-114">這可讓其腳本與執行 WPAD 引擎1.0 和2.0 版的用戶端搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a7ef8-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="a7ef8-115">範例</span><span class="sxs-lookup"><span data-stu-id="a7ef8-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="a7ef8-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7ef8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ef8-117">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="a7ef8-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="a7ef8-118">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a7ef8-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



