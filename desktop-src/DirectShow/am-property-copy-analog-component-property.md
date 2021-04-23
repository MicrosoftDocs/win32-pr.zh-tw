---
description: 查詢影片輸出是否為標準定義、類比元件影片。
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: 'AM_PROPERTY_COPY_ANALOG_COMPONENT 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6448bfbcc07be6ca37189c15c7c605887e6d22b3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910306"
---
# <a name="am_property_copy_analog_component-property"></a><span data-ttu-id="62c3d-103">AM \_ 屬性 \_ 複製 \_ 類比 \_ 元件屬性</span><span class="sxs-lookup"><span data-stu-id="62c3d-103">AM\_PROPERTY\_COPY\_ANALOG\_COMPONENT Property</span></span>

<span data-ttu-id="62c3d-104">查詢影片輸出是否為標準定義、類比元件影片。</span><span class="sxs-lookup"><span data-stu-id="62c3d-104">Queries whether the video output is standard-definition, analog component video.</span></span>



| <span data-ttu-id="62c3d-105">標籤</span><span class="sxs-lookup"><span data-stu-id="62c3d-105">Label</span></span> | <span data-ttu-id="62c3d-106">值</span><span class="sxs-lookup"><span data-stu-id="62c3d-106">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="62c3d-107">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="62c3d-107">Property Set GUID</span></span> | <span data-ttu-id="62c3d-108">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="62c3d-108">AM\_KSPROPSETID\_CopyProt</span></span>             |
| <span data-ttu-id="62c3d-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="62c3d-109">Property ID</span></span>       | <span data-ttu-id="62c3d-110">AM \_ 屬性 \_ 複製 \_ 類比 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="62c3d-110">AM\_PROPERTY\_COPY\_ANALOG\_COMPONENT</span></span> |
| <span data-ttu-id="62c3d-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="62c3d-111">Data Type</span></span>         | <span data-ttu-id="62c3d-112">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="62c3d-112">**ULONG**</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="62c3d-113">備註</span><span class="sxs-lookup"><span data-stu-id="62c3d-113">Remarks</span></span>

<span data-ttu-id="62c3d-114">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="62c3d-114">This property is read-only.</span></span>

<span data-ttu-id="62c3d-115">如果影片輸出是類比元件影片，其解析度不大於480p （針對 NTSC）或540p （適用于 PAL），則此屬性的值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="62c3d-115">The value of the property is **TRUE** if the video output is analog component video with a resolution not greater than 480p for NTSC or 540p for PAL.</span></span> <span data-ttu-id="62c3d-116">否則，此值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="62c3d-116">Otherwise, the value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c3d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="62c3d-117">Requirements</span></span>



| <span data-ttu-id="62c3d-118">需求</span><span class="sxs-lookup"><span data-stu-id="62c3d-118">Requirement</span></span> | <span data-ttu-id="62c3d-119">值</span><span class="sxs-lookup"><span data-stu-id="62c3d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c3d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="62c3d-120">Header</span></span><br/> | <dl> <span data-ttu-id="62c3d-121"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="62c3d-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c3d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62c3d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c3d-123">**DVD 禁止複製屬性集**</span><span class="sxs-lookup"><span data-stu-id="62c3d-123">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




