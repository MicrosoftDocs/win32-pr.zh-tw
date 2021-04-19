---
description: 已淘汰，不應該使用。
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: 'ADDRESS 結構 (Netmon. h) '
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999901"
---
# <a name="address-structure"></a><span data-ttu-id="0f060-103">位址結構</span><span class="sxs-lookup"><span data-stu-id="0f060-103">ADDRESS structure</span></span>

<span data-ttu-id="0f060-104">**位址** 結構已過時，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="0f060-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f060-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f060-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="0f060-106">成員</span><span class="sxs-lookup"><span data-stu-id="0f060-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f060-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="0f060-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-108">地址類型。</span><span class="sxs-lookup"><span data-stu-id="0f060-108">Address type.</span></span> <span data-ttu-id="0f060-109">它可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="0f060-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="0f060-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="0f060-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="0f060-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="0f060-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="0f060-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="0f060-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="0f060-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="0f060-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="0f060-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="0f060-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="0f060-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="0f060-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="0f060-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="0f060-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="0f060-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="0f060-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="0f060-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="0f060-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="0f060-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="0f060-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="0f060-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="0f060-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="0f060-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="0f060-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="0f060-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="0f060-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="0f060-123">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-124">以原始 MAC 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-125">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-126">以原始 IP 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-127">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-128">以原始 IPX 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-129">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-130">查看以解碼的 IPX 位址值表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-131">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-132">以原始 Vines IP 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-133">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-134">以解碼的 Vines IP 位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-135">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-136">以 Ethernet 來源位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-137">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-138">以乙太網路目的地位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-139">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-140">以 token 環形來源位址顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-141">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-142">作為權杖響鈴目的地位址的資料檢視。</span><span class="sxs-lookup"><span data-stu-id="0f060-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-143">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-144">查看以 FDDI 來源位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-145">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="0f060-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-146">查看以 FDDI 目的地位址表示的資料。</span><span class="sxs-lookup"><span data-stu-id="0f060-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="0f060-147">**旗標**</span><span class="sxs-lookup"><span data-stu-id="0f060-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0f060-148">修改位址屬性的一組旗標。</span><span class="sxs-lookup"><span data-stu-id="0f060-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f060-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f060-149">Requirements</span></span>



| <span data-ttu-id="0f060-150">需求</span><span class="sxs-lookup"><span data-stu-id="0f060-150">Requirement</span></span> | <span data-ttu-id="0f060-151">值</span><span class="sxs-lookup"><span data-stu-id="0f060-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f060-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f060-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0f060-153">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f060-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f060-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f060-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0f060-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f060-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f060-156">標頭</span><span class="sxs-lookup"><span data-stu-id="0f060-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f060-157"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="0f060-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




