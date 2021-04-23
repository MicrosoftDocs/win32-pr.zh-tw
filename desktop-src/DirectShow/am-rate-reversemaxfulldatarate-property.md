---
description: 適用于 Windows Vista 和更新版本。
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: 'AM_RATE_ReverseMaxFullDataRate 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910236"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="c4944-103">AM \_ RATE \_ ReverseMaxFullDataRate 屬性</span><span class="sxs-lookup"><span data-stu-id="c4944-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="c4944-104">適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c4944-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="c4944-105">傳回解碼器的最高反向播放速率。</span><span class="sxs-lookup"><span data-stu-id="c4944-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="c4944-106">屬性的值是最大反向速度 x 10000 的絕對值。</span><span class="sxs-lookup"><span data-stu-id="c4944-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="c4944-107">例如，如果最大的反向速度是-2.0，則此屬性的值為20000。</span><span class="sxs-lookup"><span data-stu-id="c4944-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="c4944-108">這個屬性的資料類型是 **\_ MaxFullDataRate**，其為 `typedef` **LONG**。</span><span class="sxs-lookup"><span data-stu-id="c4944-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="c4944-109">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4944-109">This property is read-only.</span></span>



| <span data-ttu-id="c4944-110">標籤</span><span class="sxs-lookup"><span data-stu-id="c4944-110">Label</span></span> | <span data-ttu-id="c4944-111">值</span><span class="sxs-lookup"><span data-stu-id="c4944-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="c4944-112">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="c4944-112">Property Set GUID</span></span> | <span data-ttu-id="c4944-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="c4944-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="c4944-114">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="c4944-114">Property ID</span></span>       | <span data-ttu-id="c4944-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="c4944-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="c4944-116">資料類型</span><span class="sxs-lookup"><span data-stu-id="c4944-116">Data Type</span></span>         | <span data-ttu-id="c4944-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="c4944-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="c4944-118">備註</span><span class="sxs-lookup"><span data-stu-id="c4944-118">Remarks</span></span>

<span data-ttu-id="c4944-119">支援順利反向播放的解碼器應該會公開此屬性。</span><span class="sxs-lookup"><span data-stu-id="c4944-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="c4944-120">如需詳細資訊，請參閱 [Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="c4944-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4944-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4944-121">Requirements</span></span>



| <span data-ttu-id="c4944-122">需求</span><span class="sxs-lookup"><span data-stu-id="c4944-122">Requirement</span></span> | <span data-ttu-id="c4944-123">值</span><span class="sxs-lookup"><span data-stu-id="c4944-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4944-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c4944-124">Header</span></span><br/> | <dl> <span data-ttu-id="c4944-125"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4944-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4944-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4944-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4944-127">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="c4944-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




