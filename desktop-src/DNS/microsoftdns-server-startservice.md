---
title: MicrosoftDNS_Server 類別的 StartService 方法
description: StartService 方法會啟動 DNS 伺服器。
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- StartService 方法 DNS
- StartService 方法 DNS，MicrosoftDNS_Server 類別
- MicrosoftDNS_Server 類別 DNS，StartService 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965729"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="b63bf-106">MicrosoftDNS 伺服器類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b63bf-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="b63bf-107">**StartService** 方法會啟動 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b63bf-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b63bf-108">語法</span><span class="sxs-lookup"><span data-stu-id="b63bf-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="b63bf-109">參數</span><span class="sxs-lookup"><span data-stu-id="b63bf-109">Parameters</span></span>

<span data-ttu-id="b63bf-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b63bf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b63bf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b63bf-111">Return value</span></span>

<span data-ttu-id="b63bf-112">錯誤 \_ 成功表示服務已順利啟動。</span><span class="sxs-lookup"><span data-stu-id="b63bf-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="b63bf-113">任何其他值都是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b63bf-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b63bf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b63bf-114">Requirements</span></span>



| <span data-ttu-id="b63bf-115">需求</span><span class="sxs-lookup"><span data-stu-id="b63bf-115">Requirement</span></span> | <span data-ttu-id="b63bf-116">值</span><span class="sxs-lookup"><span data-stu-id="b63bf-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b63bf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b63bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b63bf-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="b63bf-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b63bf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b63bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b63bf-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b63bf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b63bf-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="b63bf-121">Namespace</span></span><br/>                | <span data-ttu-id="b63bf-122">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b63bf-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b63bf-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b63bf-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b63bf-124"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="b63bf-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b63bf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b63bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b63bf-126">**MicrosoftDNS \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="b63bf-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="b63bf-127">**MicrosoftDNS 伺服器類別的 StopService 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b63bf-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="b63bf-128">**MicrosoftDNS 伺服器類別的 StartScavenging 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b63bf-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="b63bf-129">**MicrosoftDNS 伺服器類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b63bf-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





