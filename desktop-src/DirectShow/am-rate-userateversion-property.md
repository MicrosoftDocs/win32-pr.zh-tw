---
description: 這個屬性是用來指出應使用哪個版本的速率變更屬性設定。
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: 'AM_RATE_UseRateVersion 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910216"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="908a0-103">AM \_ RATE \_ UseRateVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="908a0-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="908a0-104">這個屬性是用來指出應使用哪個版本的速率變更屬性設定。</span><span class="sxs-lookup"><span data-stu-id="908a0-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="908a0-105">值是 **文字** 類型。</span><span class="sxs-lookup"><span data-stu-id="908a0-105">The value is a **WORD** type.</span></span> <span data-ttu-id="908a0-106">高序位位元組包含次要版本號碼，而低序位位元組則包含低序位位元組。</span><span class="sxs-lookup"><span data-stu-id="908a0-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="908a0-107">因此，1.1 版會以0x0101 的值發出信號。</span><span class="sxs-lookup"><span data-stu-id="908a0-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="908a0-108">如果此解碼器不支援指定的版本，它應該會使 [**IKsPropertySet：： Set**](ikspropertyset-set.md) 的呼叫失敗，並傳回 E \_ NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="908a0-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="908a0-109">如果來源篩選未設定版本，則該解碼器應預設為1.0 版。</span><span class="sxs-lookup"><span data-stu-id="908a0-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



| <span data-ttu-id="908a0-110">標籤</span><span class="sxs-lookup"><span data-stu-id="908a0-110">Label</span></span> | <span data-ttu-id="908a0-111">值</span><span class="sxs-lookup"><span data-stu-id="908a0-111">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="908a0-112">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="908a0-112">Property Set GUID</span></span> | <span data-ttu-id="908a0-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="908a0-113">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="908a0-114">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="908a0-114">Property ID</span></span>       | <span data-ttu-id="908a0-115">AM \_ RATE \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="908a0-115">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="908a0-116">資料類型</span><span class="sxs-lookup"><span data-stu-id="908a0-116">Data Type</span></span>         | <span data-ttu-id="908a0-117">**WORD**</span><span class="sxs-lookup"><span data-stu-id="908a0-117">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="908a0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="908a0-118">Requirements</span></span>



| <span data-ttu-id="908a0-119">需求</span><span class="sxs-lookup"><span data-stu-id="908a0-119">Requirement</span></span> | <span data-ttu-id="908a0-120">值</span><span class="sxs-lookup"><span data-stu-id="908a0-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="908a0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="908a0-121">Header</span></span><br/> | <dl> <span data-ttu-id="908a0-122"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="908a0-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908a0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="908a0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908a0-124">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="908a0-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




