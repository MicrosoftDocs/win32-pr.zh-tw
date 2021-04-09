---
title: 'CB_ADDRESS_TYPE 列舉 (Cbclient .h) '
description: 指定網址類別型。
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- CB_ADDRESS_TYPE 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685679"
---
# <a name="cb_address_type-enumeration"></a><span data-ttu-id="38d3a-104">CB \_ 位址 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="38d3a-104">CB\_ADDRESS\_TYPE enumeration</span></span>

<span data-ttu-id="38d3a-105">指定網址類別型。</span><span class="sxs-lookup"><span data-stu-id="38d3a-105">Specifies the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d3a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="38d3a-106">Syntax</span></span>


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="38d3a-107">常數</span><span class="sxs-lookup"><span data-stu-id="38d3a-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="38d3a-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB \_ 位址 \_ 未定義**</span><span class="sxs-lookup"><span data-stu-id="38d3a-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB\_ADDR\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="38d3a-109">網址類別型未定義。</span><span class="sxs-lookup"><span data-stu-id="38d3a-109">The address type is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="38d3a-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB \_ 位址 \_ IPv4**</span><span class="sxs-lookup"><span data-stu-id="38d3a-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB\_ADDR\_IPv4**</span></span>
</dt> <dd>

<span data-ttu-id="38d3a-111">位址是 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="38d3a-111">The address is an IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="38d3a-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB \_ 位址 \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="38d3a-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB\_ADDR\_IPv6**</span></span>
</dt> <dd>

<span data-ttu-id="38d3a-113">位址是 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="38d3a-113">The address is an IPv6 address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38d3a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="38d3a-114">Requirements</span></span>



| <span data-ttu-id="38d3a-115">需求</span><span class="sxs-lookup"><span data-stu-id="38d3a-115">Requirement</span></span> | <span data-ttu-id="38d3a-116">值</span><span class="sxs-lookup"><span data-stu-id="38d3a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38d3a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38d3a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="38d3a-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38d3a-118">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="38d3a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38d3a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="38d3a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38d3a-120">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="38d3a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="38d3a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d3a-122"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="38d3a-122"><dt>Cbclient.h</dt></span></span> </dl> |



 

 





