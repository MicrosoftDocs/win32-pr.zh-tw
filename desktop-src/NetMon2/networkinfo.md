---
description: NETWORKINFO 結構描述 NIC。
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: 'NETWORKINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695395"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="affd3-103">NETWORKINFO 結構</span><span class="sxs-lookup"><span data-stu-id="affd3-103">NETWORKINFO structure</span></span>

<span data-ttu-id="affd3-104">NETWORKINFO 結構描述 NIC。</span><span class="sxs-lookup"><span data-stu-id="affd3-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="affd3-105">語法</span><span class="sxs-lookup"><span data-stu-id="affd3-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="affd3-106">成員</span><span class="sxs-lookup"><span data-stu-id="affd3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="affd3-107">**PermanentAddr**</span><span class="sxs-lookup"><span data-stu-id="affd3-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-108">永久 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="affd3-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-109">**CurrentAddr**</span><span class="sxs-lookup"><span data-stu-id="affd3-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-110">目前的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="affd3-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="affd3-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-112">其他支援此 (的位址，例如 IP、IPX) 。</span><span class="sxs-lookup"><span data-stu-id="affd3-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="affd3-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="affd3-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-114">連結速度（以 Mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="affd3-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="affd3-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-116">媒體類型。</span><span class="sxs-lookup"><span data-stu-id="affd3-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-117">**Messagingfactorysettings.amqptransportsettings.maxframesize**</span><span class="sxs-lookup"><span data-stu-id="affd3-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-118">允許的框架大小上限。</span><span class="sxs-lookup"><span data-stu-id="affd3-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-119">**旗標**</span><span class="sxs-lookup"><span data-stu-id="affd3-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-120">此參數可以是下列其中一個資訊旗標：</span><span class="sxs-lookup"><span data-stu-id="affd3-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="affd3-121">值</span><span class="sxs-lookup"><span data-stu-id="affd3-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="affd3-122">意義</span><span class="sxs-lookup"><span data-stu-id="affd3-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="affd3-123"><dt>**\_ \_ \_ 不支援 NETWORKINFO 旗標 PMODE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="affd3-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="affd3-124">網路卡不支援混合模式，這表示它只會捕捉本質為廣播或只涉及本機電腦的流量。</span><span class="sxs-lookup"><span data-stu-id="affd3-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="affd3-125"><dt>**NETWORKINFO \_ 旗標 \_ RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="affd3-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="affd3-126">這是一張虛擬網路卡，也就是 RAS (遠端存取服務器) 透過數據機或另一張網路卡連接。</span><span class="sxs-lookup"><span data-stu-id="affd3-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="affd3-127"><dt>**NETWORKINFO \_ 旗標 \_ 遠端 \_ 卡片**</dt></span><span class="sxs-lookup"><span data-stu-id="affd3-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="affd3-128">網路卡不在本機電腦上，而是在本機電腦 bequest 的遠端電腦上進行捕獲。</span><span class="sxs-lookup"><span data-stu-id="affd3-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="affd3-129"><dt>**NETWORKINFO \_ 旗標 \_ 遠端 \_ NAL**</dt></span><span class="sxs-lookup"><span data-stu-id="affd3-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="affd3-130">目前請勿使用。</span><span class="sxs-lookup"><span data-stu-id="affd3-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="affd3-131"><dt>**\_已連線的 NETWORKINFO 旗標 \_ 遠端 \_ NAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="affd3-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="affd3-132">目前請勿使用。</span><span class="sxs-lookup"><span data-stu-id="affd3-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="affd3-133">**TimestampScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="affd3-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-134">例如，值為1表示1/1 毫秒、10表示1/10 毫秒、100表示 1/100 ms 等等。</span><span class="sxs-lookup"><span data-stu-id="affd3-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="affd3-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-136">遠端工作站的名稱。</span><span class="sxs-lookup"><span data-stu-id="affd3-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-137">**PModeSupported**</span><span class="sxs-lookup"><span data-stu-id="affd3-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-138">NIC P 模式支援指標。</span><span class="sxs-lookup"><span data-stu-id="affd3-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="affd3-139">**註解**</span><span class="sxs-lookup"><span data-stu-id="affd3-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="affd3-140">介面卡批註欄位。</span><span class="sxs-lookup"><span data-stu-id="affd3-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="affd3-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="affd3-141">Requirements</span></span>



| <span data-ttu-id="affd3-142">需求</span><span class="sxs-lookup"><span data-stu-id="affd3-142">Requirement</span></span> | <span data-ttu-id="affd3-143">值</span><span class="sxs-lookup"><span data-stu-id="affd3-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="affd3-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="affd3-144">Minimum supported client</span></span><br/> | <span data-ttu-id="affd3-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="affd3-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="affd3-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="affd3-146">Minimum supported server</span></span><br/> | <span data-ttu-id="affd3-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="affd3-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="affd3-148">標頭</span><span class="sxs-lookup"><span data-stu-id="affd3-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="affd3-149"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="affd3-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 




