---
description: 描述與標記相關聯之值的資料類型。
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: 標記類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187636"
---
# <a name="tag-types"></a><span data-ttu-id="73b64-103">標記類型</span><span class="sxs-lookup"><span data-stu-id="73b64-103">TAG Types</span></span>

<span data-ttu-id="73b64-104">描述與標記相關聯之值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="73b64-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="73b64-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="73b64-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="73b64-106">Description</span><span class="sxs-lookup"><span data-stu-id="73b64-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="73b64-107"><dt>**標記 \_輸入 \_ Null**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="73b64-108">沒有與標記相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="73b64-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="73b64-109"><dt>**標記 \_類型 \_ 位元組**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="73b64-110">**位元組** 值。</span><span class="sxs-lookup"><span data-stu-id="73b64-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="73b64-111"><dt>**標記 \_輸入 \_ WORD**</dt> <dt>0x3000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="73b64-112">**文字** 值。</span><span class="sxs-lookup"><span data-stu-id="73b64-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="73b64-113"><dt>**標記 \_輸入 \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="73b64-114">**DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="73b64-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="73b64-115"><dt>**標記 \_輸入 \_ QWORD**</dt> <dt>0x5000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="73b64-116">**ULONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="73b64-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="73b64-117"><dt>**標記 \_輸入 \_ STRINGREF**</dt> <dt>0x6000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="73b64-118">Token 化的字串值。</span><span class="sxs-lookup"><span data-stu-id="73b64-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="73b64-119"><dt>**標記 \_類型 \_ 清單**</dt> <dt>0x7000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="73b64-120">標記值的清單。</span><span class="sxs-lookup"><span data-stu-id="73b64-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="73b64-121"><dt>**標記 \_類型 \_ 字串**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="73b64-122">字串值。</span><span class="sxs-lookup"><span data-stu-id="73b64-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="73b64-123"><dt>**標記 \_輸入 \_ BINARY**</dt> <dt>0x9000</dt></span><span class="sxs-lookup"><span data-stu-id="73b64-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="73b64-124">二進位值。</span><span class="sxs-lookup"><span data-stu-id="73b64-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="73b64-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="73b64-125">Requirements</span></span>



| <span data-ttu-id="73b64-126">需求</span><span class="sxs-lookup"><span data-stu-id="73b64-126">Requirement</span></span> | <span data-ttu-id="73b64-127">值</span><span class="sxs-lookup"><span data-stu-id="73b64-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73b64-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73b64-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73b64-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73b64-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73b64-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73b64-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73b64-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73b64-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73b64-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73b64-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b64-133">**標記**</span><span class="sxs-lookup"><span data-stu-id="73b64-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="73b64-134">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="73b64-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="73b64-135">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="73b64-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




