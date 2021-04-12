---
title: 'CB_TARGET_INFO 結構 (Cbclient .h) '
description: 包含目的電腦的相關資訊，以及應重新導向連入連接的 IP 位址。
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO 結構遠端桌面服務
- PCB_TARGET_INFO 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384210"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="d5ede-105">CB \_ 目標 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="d5ede-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="d5ede-106">包含目的電腦的相關資訊，以及應重新導向連入連接的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d5ede-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="d5ede-107">此結構會搭配 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="d5ede-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ede-108">語法</span><span class="sxs-lookup"><span data-stu-id="d5ede-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="d5ede-109">成員</span><span class="sxs-lookup"><span data-stu-id="d5ede-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5ede-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="d5ede-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="d5ede-111">代表目標伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d5ede-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="d5ede-112">針對遠端桌面虛擬化 (RDV) 案例，此成員為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d5ede-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="d5ede-113">針對 (RDSH) 案例的遠端桌面工作階段主機，此成員包含重新導向連入連線的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d5ede-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="d5ede-114">**AddressCount**</span><span class="sxs-lookup"><span data-stu-id="d5ede-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="d5ede-115">**位址** 陣列中的有效專案數。</span><span class="sxs-lookup"><span data-stu-id="d5ede-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="d5ede-116">**位址**</span><span class="sxs-lookup"><span data-stu-id="d5ede-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="d5ede-117">字串陣列，包含重新導向連入連接的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d5ede-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="d5ede-118">這個陣列中的有效元素數目是在 **AddressCount** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="d5ede-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5ede-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5ede-119">Requirements</span></span>



| <span data-ttu-id="d5ede-120">需求</span><span class="sxs-lookup"><span data-stu-id="d5ede-120">Requirement</span></span> | <span data-ttu-id="d5ede-121">值</span><span class="sxs-lookup"><span data-stu-id="d5ede-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ede-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5ede-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ede-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5ede-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="d5ede-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5ede-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ede-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5ede-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="d5ede-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d5ede-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5ede-127"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ede-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ede-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5ede-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ede-129">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="d5ede-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





