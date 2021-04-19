---
description: 查詢影片輸出是否為標準定義、類比元件影片。
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: 'AM_PROPERTY_COPY_ANALOG_COMPONENT 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3998156bf372c39018aa73ba30a661117519c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996403"
---
# <a name="am_property_copy_analog_component-property"></a><span data-ttu-id="92dc5-103">AM \_ 屬性 \_ 複製 \_ 類比 \_ 元件屬性</span><span class="sxs-lookup"><span data-stu-id="92dc5-103">AM\_PROPERTY\_COPY\_ANALOG\_COMPONENT Property</span></span>

<span data-ttu-id="92dc5-104">查詢影片輸出是否為標準定義、類比元件影片。</span><span class="sxs-lookup"><span data-stu-id="92dc5-104">Queries whether the video output is standard-definition, analog component video.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="92dc5-105">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="92dc5-105">Property Set GUID</span></span> | <span data-ttu-id="92dc5-106">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="92dc5-106">AM\_KSPROPSETID\_CopyProt</span></span>             |
| <span data-ttu-id="92dc5-107">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="92dc5-107">Property ID</span></span>       | <span data-ttu-id="92dc5-108">AM \_ 屬性 \_ 複製 \_ 類比 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="92dc5-108">AM\_PROPERTY\_COPY\_ANALOG\_COMPONENT</span></span> |
| <span data-ttu-id="92dc5-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="92dc5-109">Data Type</span></span>         | <span data-ttu-id="92dc5-110">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="92dc5-110">**ULONG**</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="92dc5-111">備註</span><span class="sxs-lookup"><span data-stu-id="92dc5-111">Remarks</span></span>

<span data-ttu-id="92dc5-112">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="92dc5-112">This property is read-only.</span></span>

<span data-ttu-id="92dc5-113">如果影片輸出是類比元件影片，其解析度不大於480p （針對 NTSC）或540p （適用于 PAL），則此屬性的值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="92dc5-113">The value of the property is **TRUE** if the video output is analog component video with a resolution not greater than 480p for NTSC or 540p for PAL.</span></span> <span data-ttu-id="92dc5-114">否則，此值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="92dc5-114">Otherwise, the value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92dc5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="92dc5-115">Requirements</span></span>



| <span data-ttu-id="92dc5-116">需求</span><span class="sxs-lookup"><span data-stu-id="92dc5-116">Requirement</span></span> | <span data-ttu-id="92dc5-117">值</span><span class="sxs-lookup"><span data-stu-id="92dc5-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92dc5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="92dc5-118">Header</span></span><br/> | <dl> <span data-ttu-id="92dc5-119"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="92dc5-119"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92dc5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92dc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92dc5-121">**DVD 禁止複製屬性集**</span><span class="sxs-lookup"><span data-stu-id="92dc5-121">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




