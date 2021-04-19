---
description: Windows 可攜式裝置支援下列常見的資訊屬性。
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: '一般資訊屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000889"
---
# <a name="common-information-properties"></a><span data-ttu-id="3a94f-103">一般資訊屬性</span><span class="sxs-lookup"><span data-stu-id="3a94f-103">Common Information Properties</span></span>

<span data-ttu-id="3a94f-104">Windows 可攜式裝置支援下列常見的資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="3a94f-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="3a94f-105">屬性</span><span class="sxs-lookup"><span data-stu-id="3a94f-105">Property</span></span>                                      | <span data-ttu-id="3a94f-106">VarType</span><span class="sxs-lookup"><span data-stu-id="3a94f-106">VarType</span></span>        | <span data-ttu-id="3a94f-107">Description</span><span class="sxs-lookup"><span data-stu-id="3a94f-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a94f-108">**WPD \_ 一般 \_ 資訊 \_ 注意事項**</span><span class="sxs-lookup"><span data-stu-id="3a94f-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="3a94f-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3a94f-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3a94f-110">對於約會、工作和類似的物件，此屬性包含指定物件的任何附注。</span><span class="sxs-lookup"><span data-stu-id="3a94f-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="3a94f-111">**WPD \_ 一般 \_ 資訊 \_ 主體**</span><span class="sxs-lookup"><span data-stu-id="3a94f-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="3a94f-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3a94f-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3a94f-113">值，指定這個物件的主旨欄位。</span><span class="sxs-lookup"><span data-stu-id="3a94f-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="3a94f-114">**WPD \_ 一般 \_ 資訊 \_ 主體 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="3a94f-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="3a94f-115">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3a94f-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3a94f-116">這個屬性包含純文字或 HTML 格式之物件的內文文字。</span><span class="sxs-lookup"><span data-stu-id="3a94f-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="3a94f-117">**WPD \_ 一般 \_ 資訊 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="3a94f-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="3a94f-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="3a94f-118">**VT\_UI4**</span></span>    | <span data-ttu-id="3a94f-119">值，指定這個物件的優先權。</span><span class="sxs-lookup"><span data-stu-id="3a94f-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="3a94f-120">0表示最高優先順序。</span><span class="sxs-lookup"><span data-stu-id="3a94f-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="3a94f-121">**WPD \_ 一般 \_ 資訊 \_ 開始 \_ 日期時間**</span><span class="sxs-lookup"><span data-stu-id="3a94f-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="3a94f-122">**VT \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="3a94f-122">**VT\_DATE**</span></span>   | <span data-ttu-id="3a94f-123">值，指定約會、工作或類似物件排定開始的日期/時間。</span><span class="sxs-lookup"><span data-stu-id="3a94f-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="3a94f-124">**WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME**</span><span class="sxs-lookup"><span data-stu-id="3a94f-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="3a94f-125">**VT \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="3a94f-125">**VT\_DATE**</span></span>   | <span data-ttu-id="3a94f-126">值，指定約會、工作或類似物件排定結束的日期/時間。</span><span class="sxs-lookup"><span data-stu-id="3a94f-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="3a94f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a94f-127">Requirements</span></span>



| <span data-ttu-id="3a94f-128">需求</span><span class="sxs-lookup"><span data-stu-id="3a94f-128">Requirement</span></span> | <span data-ttu-id="3a94f-129">值</span><span class="sxs-lookup"><span data-stu-id="3a94f-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a94f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3a94f-130">Header</span></span><br/> | <dl> <span data-ttu-id="3a94f-131"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a94f-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a94f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a94f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a94f-133">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="3a94f-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




