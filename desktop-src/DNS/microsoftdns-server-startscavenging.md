---
title: MicrosoftDNS_Server 類別的 StartScavenging 方法
description: StartScavenging 方法會開始清除要清除之區域中的過時記錄。
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- StartScavenging 方法 DNS
- StartScavenging 方法 DNS，MicrosoftDNS_Server 類別
- MicrosoftDNS_Server 類別 DNS，StartScavenging 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934526"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="e7a0f-106">MicrosoftDNS 伺服器類別的 StartScavenging 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e7a0f-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="e7a0f-107">**StartScavenging** 方法會開始清除要清除之區域中的過時記錄。</span><span class="sxs-lookup"><span data-stu-id="e7a0f-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a0f-108">語法</span><span class="sxs-lookup"><span data-stu-id="e7a0f-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="e7a0f-109">參數</span><span class="sxs-lookup"><span data-stu-id="e7a0f-109">Parameters</span></span>

<span data-ttu-id="e7a0f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e7a0f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7a0f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7a0f-111">Return value</span></span>

<span data-ttu-id="e7a0f-112">錯誤 \_ 成功表示清除已順利啟動。</span><span class="sxs-lookup"><span data-stu-id="e7a0f-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="e7a0f-113">任何其他值都是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e7a0f-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a0f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7a0f-114">Requirements</span></span>



| <span data-ttu-id="e7a0f-115">需求</span><span class="sxs-lookup"><span data-stu-id="e7a0f-115">Requirement</span></span> | <span data-ttu-id="e7a0f-116">值</span><span class="sxs-lookup"><span data-stu-id="e7a0f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a0f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7a0f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a0f-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="e7a0f-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e7a0f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7a0f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a0f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7a0f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e7a0f-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="e7a0f-121">Namespace</span></span><br/>                | <span data-ttu-id="e7a0f-122">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e7a0f-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e7a0f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e7a0f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7a0f-124"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7a0f-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a0f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7a0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a0f-126">**MicrosoftDNS \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="e7a0f-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="e7a0f-127">**MicrosoftDNS 伺服器類別的 StartService 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a0f-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="e7a0f-128">**MicrosoftDNS 伺服器類別的 StopService 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a0f-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="e7a0f-129">**MicrosoftDNS 伺服器類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a0f-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





