---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB IDL 定義
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104316705"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="6599d-103">ODJ_WIN7BLOB 結構</span><span class="sxs-lookup"><span data-stu-id="6599d-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="6599d-104">包含將用戶端加入網域所需的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="6599d-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="6599d-105">語法</span><span class="sxs-lookup"><span data-stu-id="6599d-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="6599d-106">成員</span><span class="sxs-lookup"><span data-stu-id="6599d-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="6599d-107">lpDomain</span><span class="sxs-lookup"><span data-stu-id="6599d-107">lpDomain</span></span>

<span data-ttu-id="6599d-108">必須設定為功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="6599d-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="6599d-109">lpMachineName</span><span class="sxs-lookup"><span data-stu-id="6599d-109">lpMachineName</span></span>

<span data-ttu-id="6599d-110">必須設定為電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="6599d-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="6599d-111">lpMachinePassword</span><span class="sxs-lookup"><span data-stu-id="6599d-111">lpMachinePassword</span></span>

<span data-ttu-id="6599d-112">必須針對 lpMachineName 所識別的電腦帳戶設定為純文字密碼</span><span class="sxs-lookup"><span data-stu-id="6599d-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="6599d-113">DnsDomainInfo</span><span class="sxs-lookup"><span data-stu-id="6599d-113">DnsDomainInfo</span></span>

<span data-ttu-id="6599d-114">包含要聯結之網域的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6599d-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="6599d-115">DcInfo</span><span class="sxs-lookup"><span data-stu-id="6599d-115">DcInfo</span></span>

<span data-ttu-id="6599d-116">包含用來建立電腦帳戶 Active Directory 之網域控制站的命名和定址資訊。</span><span class="sxs-lookup"><span data-stu-id="6599d-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="6599d-117">選項</span><span class="sxs-lookup"><span data-stu-id="6599d-117">Options</span></span>

<span data-ttu-id="6599d-118">必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="6599d-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="6599d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6599d-119">See also</span></span>

[<span data-ttu-id="6599d-120">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="6599d-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="6599d-121">**ODJ \_ 原則 \_ DNS \_ 網域 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6599d-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="6599d-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="6599d-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



