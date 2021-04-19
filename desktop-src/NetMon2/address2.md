---
description: 包含任何類型之支援位址的單一位址。
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: " (Netmon. h) 的位址2結構"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978953"
---
# <a name="address2-structure"></a><span data-ttu-id="201ad-103">位址2結構</span><span class="sxs-lookup"><span data-stu-id="201ad-103">ADDRESS2 structure</span></span>

<span data-ttu-id="201ad-104">**位址** 結構包含任何類型之支援位址的單一位址。</span><span class="sxs-lookup"><span data-stu-id="201ad-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="201ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="201ad-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="201ad-106">成員</span><span class="sxs-lookup"><span data-stu-id="201ad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="201ad-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="201ad-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-108">地址類型。</span><span class="sxs-lookup"><span data-stu-id="201ad-108">Address type.</span></span> <span data-ttu-id="201ad-109">它可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="201ad-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="201ad-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="201ad-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="201ad-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="201ad-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="201ad-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="201ad-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="201ad-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="201ad-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="201ad-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="201ad-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="201ad-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="201ad-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="201ad-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="201ad-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="201ad-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="201ad-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="201ad-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="201ad-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="201ad-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="201ad-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="201ad-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="201ad-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="201ad-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="201ad-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="201ad-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="201ad-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="201ad-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="201ad-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="201ad-124">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-125">以原始 MAC 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-126">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-127">以原始 IP 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="201ad-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-129">以原始 IP 第6版位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-130">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-131">以原始 IPX 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-132">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-133">查看以解碼的 IPX 位址值表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-134">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-135">以原始 Vines IP 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-136">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-137">以解碼的 Vines IP 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-138">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-139">以 Ethernet 來源位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-140">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-141">以乙太網路目的地位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-142">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-143">以 token 環形來源位址顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-144">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-145">作為權杖響鈴目的地位址的資料檢視。</span><span class="sxs-lookup"><span data-stu-id="201ad-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-146">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-147">查看以 FDDI 來源位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-148">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="201ad-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="201ad-149">查看以 FDDI 目的地位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="201ad-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="201ad-150">**旗標**</span><span class="sxs-lookup"><span data-stu-id="201ad-150">**Flags**</span></span>
<span data-ttu-id="201ad-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="201ad-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="201ad-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="201ad-152">Requirements</span></span>



| <span data-ttu-id="201ad-153">需求</span><span class="sxs-lookup"><span data-stu-id="201ad-153">Requirement</span></span> | <span data-ttu-id="201ad-154">值</span><span class="sxs-lookup"><span data-stu-id="201ad-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="201ad-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="201ad-155">Minimum supported client</span></span><br/> | <span data-ttu-id="201ad-156">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="201ad-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="201ad-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="201ad-157">Minimum supported server</span></span><br/> | <span data-ttu-id="201ad-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="201ad-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="201ad-159">標頭</span><span class="sxs-lookup"><span data-stu-id="201ad-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="201ad-160"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="201ad-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




