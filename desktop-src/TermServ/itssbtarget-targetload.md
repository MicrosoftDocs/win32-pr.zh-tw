---
title: ITsSbTarget TargetLoad 屬性
description: 抓取目標的相對負載。
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- TargetLoad 屬性遠端桌面服務
- TargetLoad 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，TargetLoad 屬性
- TargetLoad 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，TargetLoad 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678588"
---
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="bdc02-108">ITsSbTarget：： TargetLoad 屬性</span><span class="sxs-lookup"><span data-stu-id="bdc02-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="bdc02-109">抓取目標的相對負載。</span><span class="sxs-lookup"><span data-stu-id="bdc02-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="bdc02-110">此值是以現有和擱置中會話的數目為基礎。</span><span class="sxs-lookup"><span data-stu-id="bdc02-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="bdc02-111">根據預設，暫止的會話與現有的會話具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="bdc02-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="bdc02-112">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bdc02-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc02-113">語法</span><span class="sxs-lookup"><span data-stu-id="bdc02-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="bdc02-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="bdc02-114">Property value</span></span>

<span data-ttu-id="bdc02-115">代表目標相關負載的數位。</span><span class="sxs-lookup"><span data-stu-id="bdc02-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc02-116">備註</span><span class="sxs-lookup"><span data-stu-id="bdc02-116">Remarks</span></span>

<span data-ttu-id="bdc02-117">您可以藉由設定連線代理人的 *LB \_ ConnectionEstablishmentPenalty* 參數值，來變更相對於作用中會話的暫止會話加權。</span><span class="sxs-lookup"><span data-stu-id="bdc02-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="bdc02-118">此參數位於 **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** 登錄機碼底下。</span><span class="sxs-lookup"><span data-stu-id="bdc02-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="bdc02-119">預設值為1，表示擱置會話的加權與作用中會話的加權相同。</span><span class="sxs-lookup"><span data-stu-id="bdc02-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="bdc02-120">這個屬性可在已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2 上取得，並安裝在 [**ITsSbTargetEx**](itssbtargetex.md) 介面中。</span><span class="sxs-lookup"><span data-stu-id="bdc02-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc02-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdc02-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bdc02-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdc02-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="bdc02-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="bdc02-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdc02-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdc02-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="bdc02-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bdc02-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdc02-126">Idl</span><span class="sxs-lookup"><span data-stu-id="bdc02-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="bdc02-127"><dt>Sbtsv .idl</dt> </span><span class="sxs-lookup"><span data-stu-id="bdc02-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdc02-128">IID</span><span class="sxs-lookup"><span data-stu-id="bdc02-128">IID</span></span><br/></td>
<td><span data-ttu-id="bdc02-129">IID_ITsSbTarget 定義為：</span><span class="sxs-lookup"><span data-stu-id="bdc02-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="bdc02-130">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="bdc02-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="bdc02-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdc02-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="bdc02-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdc02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc02-133">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="bdc02-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="bdc02-134">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="bdc02-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





