---
description: Windows 可攜式裝置支援下列約會屬性。
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: '約會屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996447"
---
# <a name="appointment-properties"></a><span data-ttu-id="c4ecc-103">約會屬性</span><span class="sxs-lookup"><span data-stu-id="c4ecc-103">Appointment Properties</span></span>

<span data-ttu-id="c4ecc-104">Windows 可攜式裝置支援下列約會屬性。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="c4ecc-105">屬性</span><span class="sxs-lookup"><span data-stu-id="c4ecc-105">Property</span></span>                                   | <span data-ttu-id="c4ecc-106">VarType</span><span class="sxs-lookup"><span data-stu-id="c4ecc-106">VarType</span></span>        | <span data-ttu-id="c4ecc-107">Description</span><span class="sxs-lookup"><span data-stu-id="c4ecc-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ecc-108">**WPD \_ 約會已 \_ 接受 \_ 出席者**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="c4ecc-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-110">已接受約會的參與者清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="c4ecc-111">**WPD \_ 約會已 \_ 拒絕 \_ 出席者**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="c4ecc-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-113">已拒絕約會的參與者清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="c4ecc-114">**WPD \_ 約會 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="c4ecc-115">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c4ecc-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="c4ecc-116">約會的讀取者易記位置，例如「建立5，房間7」。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="c4ecc-117">**WPD \_ 預約 \_ 選用 \_ 出席者**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="c4ecc-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-119">約會的選用出席者清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="c4ecc-120">**WPD \_ 預約 \_ 必填 \_ 出席者**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="c4ecc-121">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-122">約會的必要出席者清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="c4ecc-123">**WPD \_ 約會 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="c4ecc-124">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-125">約會所需資源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="c4ecc-126">**WPD \_ 約會 \_ 暫時 \_ 出席者**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="c4ecc-127">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-128">暫時接受約會的出席者清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="c4ecc-129">**WPD \_ 約會 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="c4ecc-130">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c4ecc-131">約會的類型，例如「個人」、「商務」等等。</span><span class="sxs-lookup"><span data-stu-id="c4ecc-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="c4ecc-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4ecc-132">Requirements</span></span>



| <span data-ttu-id="c4ecc-133">需求</span><span class="sxs-lookup"><span data-stu-id="c4ecc-133">Requirement</span></span> | <span data-ttu-id="c4ecc-134">值</span><span class="sxs-lookup"><span data-stu-id="c4ecc-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ecc-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c4ecc-135">Header</span></span><br/> | <dl> <span data-ttu-id="c4ecc-136"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ecc-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ecc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4ecc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ecc-138">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="c4ecc-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




