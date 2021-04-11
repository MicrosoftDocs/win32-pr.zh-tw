---
title: ITsSbTarget TargetName 屬性
description: 指定或抓取目標的名稱。
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- TargetName 屬性遠端桌面服務
- TargetName 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，TargetName 屬性
- TargetName 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，TargetName 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022653"
---
# <a name="itssbtargettargetname-property"></a><span data-ttu-id="36865-108">ITsSbTarget：： TargetName 屬性</span><span class="sxs-lookup"><span data-stu-id="36865-108">ITsSbTarget::TargetName property</span></span>

<span data-ttu-id="36865-109">指定或抓取目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="36865-109">Specifies or retrieves the name of the target.</span></span>

<span data-ttu-id="36865-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="36865-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="36865-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="36865-111">Syntax</span></span>


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="36865-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="36865-112">Property value</span></span>

<span data-ttu-id="36865-113">指定目標名稱的 **BSTR** 變數。</span><span class="sxs-lookup"><span data-stu-id="36865-113">A **BSTR** variable that specifies the target name.</span></span>

## <a name="remarks"></a><span data-ttu-id="36865-114">備註</span><span class="sxs-lookup"><span data-stu-id="36865-114">Remarks</span></span>

<span data-ttu-id="36865-115">在 Windows Server 2012 之前，此屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="36865-115">This property was read-only prior to Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="36865-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="36865-116">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36865-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36865-117">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="36865-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="36865-118">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36865-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36865-119">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="36865-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36865-120">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36865-121">Idl</span><span class="sxs-lookup"><span data-stu-id="36865-121">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="36865-122"><dt>Sbtsv .idl</dt> </span><span class="sxs-lookup"><span data-stu-id="36865-122"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36865-123">IID</span><span class="sxs-lookup"><span data-stu-id="36865-123">IID</span></span><br/></td>
<td><span data-ttu-id="36865-124">IID_ITsSbTarget 定義為：</span><span class="sxs-lookup"><span data-stu-id="36865-124">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="36865-125">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="36865-125">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="36865-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36865-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="36865-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36865-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36865-128">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="36865-128">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="36865-129">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="36865-129">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





