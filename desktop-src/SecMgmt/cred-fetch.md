---
description: 定義值，決定如何提取群組受管理的服務帳戶 (gMSA) 的認證。
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: 'CRED_FETCH 列舉 (Secpkg .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944754"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="b2da4-103">認證 \_ 提取列舉</span><span class="sxs-lookup"><span data-stu-id="b2da4-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="b2da4-104">定義值，決定如何提取群組受管理的服務帳戶 (gMSA) 的認證。</span><span class="sxs-lookup"><span data-stu-id="b2da4-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2da4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2da4-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="b2da4-106">常數</span><span class="sxs-lookup"><span data-stu-id="b2da4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b2da4-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span><span class="sxs-lookup"><span data-stu-id="b2da4-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="b2da4-108">表示作業系統應該先嘗試從本機快取取出密碼。</span><span class="sxs-lookup"><span data-stu-id="b2da4-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="b2da4-109">如果需要取得密碼，則作業系統應聯繫網域控制站以取得密碼。</span><span class="sxs-lookup"><span data-stu-id="b2da4-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="b2da4-110">如果失敗，則會傳回狀態為 success 的任何快取密碼。</span><span class="sxs-lookup"><span data-stu-id="b2da4-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="b2da4-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span><span class="sxs-lookup"><span data-stu-id="b2da4-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="b2da4-112">將本機 DPAPI 認證傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="b2da4-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="b2da4-113"> (Ssp) 的 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly)通常不需要使用此列舉。</span><span class="sxs-lookup"><span data-stu-id="b2da4-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b2da4-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span><span class="sxs-lookup"><span data-stu-id="b2da4-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="b2da4-115">強制作業系統嘗試從網域控制站讀取密碼。</span><span class="sxs-lookup"><span data-stu-id="b2da4-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="b2da4-116">在密碼變換期間，網域控制站和其他成員主機上的密碼可能已變更，但 gMSA 成員主機會將密碼識別為有效。</span><span class="sxs-lookup"><span data-stu-id="b2da4-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="b2da4-117">這種情況可能是因為不同網域控制站之間的時鐘誤差問題所造成。</span><span class="sxs-lookup"><span data-stu-id="b2da4-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="b2da4-118">當指定這個值時，作業系統會判斷是否可能因為時鐘誤差而可能變更密碼，如果是，則會抓取密碼。</span><span class="sxs-lookup"><span data-stu-id="b2da4-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="b2da4-119">否則會傳回快取的認證。</span><span class="sxs-lookup"><span data-stu-id="b2da4-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="b2da4-120">如果沒有快取的認證，則作業系統會嘗試從網域控制站取得一個。</span><span class="sxs-lookup"><span data-stu-id="b2da4-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2da4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2da4-121">Requirements</span></span>



| <span data-ttu-id="b2da4-122">需求</span><span class="sxs-lookup"><span data-stu-id="b2da4-122">Requirement</span></span> | <span data-ttu-id="b2da4-123">值</span><span class="sxs-lookup"><span data-stu-id="b2da4-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2da4-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2da4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2da4-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2da4-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2da4-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2da4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2da4-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2da4-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b2da4-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b2da4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2da4-129"><dt>Secpkg。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2da4-129"><dt>Secpkg.h</dt></span></span> </dl> |



 

