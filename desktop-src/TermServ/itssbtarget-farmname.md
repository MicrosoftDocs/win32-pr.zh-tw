---
title: ITsSbTarget FarmName 屬性
description: 抓取或指定此目標所聯結的伺服器陣列名稱。
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- FarmName 屬性遠端桌面服務
- FarmName 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，FarmName 屬性
- FarmName 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，FarmName 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678412"
---
# <a name="itssbtargetfarmname-property"></a><span data-ttu-id="31347-108">ITsSbTarget：： FarmName 屬性</span><span class="sxs-lookup"><span data-stu-id="31347-108">ITsSbTarget::FarmName property</span></span>

<span data-ttu-id="31347-109">抓取或指定此目標所聯結的伺服器陣列名稱。</span><span class="sxs-lookup"><span data-stu-id="31347-109">Retrieves or specifies the name of the farm to which this target is joined.</span></span>

<span data-ttu-id="31347-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="31347-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31347-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="31347-111">Syntax</span></span>


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="31347-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="31347-112">Property value</span></span>

<span data-ttu-id="31347-113">包含伺服器陣列名稱的 **BSTR** 變數。</span><span class="sxs-lookup"><span data-stu-id="31347-113">A **BSTR** variable that contains the farm name.</span></span>

## <a name="requirements"></a><span data-ttu-id="31347-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="31347-114">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31347-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31347-115">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="31347-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="31347-116">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31347-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31347-117">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="31347-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="31347-118">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31347-119">Idl</span><span class="sxs-lookup"><span data-stu-id="31347-119">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="31347-120"><dt>Sbtsv .idl</dt> </span><span class="sxs-lookup"><span data-stu-id="31347-120"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31347-121">IID</span><span class="sxs-lookup"><span data-stu-id="31347-121">IID</span></span><br/></td>
<td><span data-ttu-id="31347-122">IID_ITsSbTarget 定義為：</span><span class="sxs-lookup"><span data-stu-id="31347-122">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="31347-123">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="31347-123">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="31347-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31347-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="31347-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31347-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31347-126">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="31347-126">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="31347-127">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="31347-127">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





