---
title: 'RAS_PPP_PROJECTION_RESULT 結構 (Rassapi .h) '
description: RAS \_ ppp \_ 投射 \_ 結果結構是用來報告埠之各種 PPP 投影作業的結果。
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685981"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="70eb2-104">RAS \_ PPP \_ 投射 \_ 結果結構</span><span class="sxs-lookup"><span data-stu-id="70eb2-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="70eb2-105">\[Windows Vista 不支援 **RAS \_ PPP \_ 投射 \_ 結果** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="70eb2-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="70eb2-106">**RAS \_ ppp \_ 投射 \_ 結果** 結構是用來報告埠之各種 PPP 投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="70eb2-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="70eb2-107">語法</span><span class="sxs-lookup"><span data-stu-id="70eb2-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="70eb2-108">成員</span><span class="sxs-lookup"><span data-stu-id="70eb2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70eb2-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="70eb2-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="70eb2-110">此為 [**RAS \_ ppp \_ NBFCP \_ 結果**](ras-ppp-nbfcp-result-str.md) 結構，會報告 PPP NetBEUI Framer (NBF) 投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="70eb2-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="70eb2-111">**Ip**</span><span class="sxs-lookup"><span data-stu-id="70eb2-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="70eb2-112">[**RAS \_ ppp \_ IPCP \_ 結果**](ras-ppp-ipcp-result-str.md)結構，會報告 PPP 網際網路通訊協定 (IP) 投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="70eb2-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="70eb2-113">**Ipx**</span><span class="sxs-lookup"><span data-stu-id="70eb2-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="70eb2-114">[**RAS \_ ppp \_ IPXCP \_ 結果**](ras-ppp-ipxcp-result-str.md)結構，會報告 PPP 網際網路封包交換 (IPX) 投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="70eb2-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="70eb2-115">**at**</span><span class="sxs-lookup"><span data-stu-id="70eb2-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="70eb2-116">[**RAS \_ PPP 的 \_ ATCP \_ 結果**](ras-ppp-atcp-result-str.md)結構。</span><span class="sxs-lookup"><span data-stu-id="70eb2-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70eb2-117">備註</span><span class="sxs-lookup"><span data-stu-id="70eb2-117">Remarks</span></span>

<span data-ttu-id="70eb2-118">此結構會報告 NetBEUI、TCP/IP 和 IPX 通訊協定的投射結果。</span><span class="sxs-lookup"><span data-stu-id="70eb2-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="70eb2-119">每個 PPP 結構都有一個 **dwError** 成員，指出結構中的其他資訊是否有效。</span><span class="sxs-lookup"><span data-stu-id="70eb2-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="70eb2-120">如果 **DWERROR** 沒有 \_ 錯誤，則其他資訊是有效的。</span><span class="sxs-lookup"><span data-stu-id="70eb2-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="70eb2-121">如果 **dwError** 是 winerror.h. h 或 Raserror 中的其中一個錯誤碼，則其他資訊無效。</span><span class="sxs-lookup"><span data-stu-id="70eb2-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="70eb2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="70eb2-122">Requirements</span></span>



| <span data-ttu-id="70eb2-123">需求</span><span class="sxs-lookup"><span data-stu-id="70eb2-123">Requirement</span></span> | <span data-ttu-id="70eb2-124">值</span><span class="sxs-lookup"><span data-stu-id="70eb2-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="70eb2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70eb2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="70eb2-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70eb2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="70eb2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70eb2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="70eb2-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70eb2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="70eb2-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="70eb2-129">End of client support</span></span><br/>    | <span data-ttu-id="70eb2-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="70eb2-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="70eb2-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="70eb2-131">End of server support</span></span><br/>    | <span data-ttu-id="70eb2-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="70eb2-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="70eb2-133">標頭</span><span class="sxs-lookup"><span data-stu-id="70eb2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="70eb2-134"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="70eb2-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70eb2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70eb2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70eb2-136">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="70eb2-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="70eb2-137">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="70eb2-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="70eb2-138">**RAS \_ 埠 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="70eb2-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="70eb2-139">**RAS \_ PPP \_ ATCP \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="70eb2-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="70eb2-140">**RAS \_ PPP \_ IPCP \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="70eb2-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="70eb2-141">**RAS \_ PPP \_ IPXCP \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="70eb2-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="70eb2-142">**RAS \_ PPP \_ NBFCP \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="70eb2-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="70eb2-143">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="70eb2-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





