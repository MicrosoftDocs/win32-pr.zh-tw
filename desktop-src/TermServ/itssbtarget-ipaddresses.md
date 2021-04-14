---
title: ITsSbTarget IpAddresses 屬性
description: 捕獲或指定目標的外部 IP 位址。
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- TargetExternalIpAddresses 屬性遠端桌面服務
- TargetExternalIpAddresses 屬性遠端桌面服務，ITsSbTarget 介面
- TargetExternalIpAddresses 屬性遠端桌面服務，ITsSbTarget 介面
- IpAddresses 屬性遠端桌面服務
- IpAddresses 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，IpAddresses 屬性
- IpAddresses 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，IpAddresses 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373006"
---
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="77df8-111">ITsSbTarget：： IpAddresses 屬性</span><span class="sxs-lookup"><span data-stu-id="77df8-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="77df8-112">捕獲或指定目標的外部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="77df8-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="77df8-113">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="77df8-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="77df8-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="77df8-114">Syntax</span></span>


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="77df8-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="77df8-115">Property value</span></span>

<span data-ttu-id="77df8-116">[**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)結構陣列的指標，此陣列會接收目標的外部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="77df8-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="77df8-117">**DWORD** 變數的指標，其中包含 *sockaddr* 參數中的外部 IP 位址數目。</span><span class="sxs-lookup"><span data-stu-id="77df8-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="77df8-118">如果位址數目不明，請將 *sockaddr* 傳遞為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="77df8-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="77df8-119">方法會傳回在 *sockaddr* 參數所指向的陣列中配置所需的 [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)結構數目。</span><span class="sxs-lookup"><span data-stu-id="77df8-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="77df8-120">備註</span><span class="sxs-lookup"><span data-stu-id="77df8-120">Remarks</span></span>

<span data-ttu-id="77df8-121">此屬性在 Windows Server 2008 R2 中先前稱為 **TargetExternalIpAddresses** 。</span><span class="sxs-lookup"><span data-stu-id="77df8-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="77df8-122">如果外部 IP 位址的數目未知，您可以呼叫這個方法，並將 *sockaddr* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="77df8-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="77df8-123">方法接著會在 *numAddresses* 參數中傳回接收所有外部 IP 位址所需的 [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) 結構數目。</span><span class="sxs-lookup"><span data-stu-id="77df8-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="77df8-124">根據此數位配置 *sockaddr* 的陣列，然後再次呼叫方法，將 *sockaddr* 設定為新配置的陣列，並 *numAddresses* 至第一個呼叫傳回的數位。</span><span class="sxs-lookup"><span data-stu-id="77df8-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="77df8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="77df8-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77df8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77df8-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="77df8-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="77df8-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77df8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77df8-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="77df8-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77df8-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77df8-130">Idl</span><span class="sxs-lookup"><span data-stu-id="77df8-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="77df8-131"><dt>Sbtsv .idl</dt> </span><span class="sxs-lookup"><span data-stu-id="77df8-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77df8-132">IID</span><span class="sxs-lookup"><span data-stu-id="77df8-132">IID</span></span><br/></td>
<td><span data-ttu-id="77df8-133">IID_ITsSbTarget 定義為：</span><span class="sxs-lookup"><span data-stu-id="77df8-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="77df8-134">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="77df8-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="77df8-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77df8-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="77df8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77df8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77df8-137">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="77df8-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="77df8-138">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="77df8-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="77df8-139">**TSSD \_ ConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="77df8-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





