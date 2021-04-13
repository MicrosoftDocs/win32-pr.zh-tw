---
title: 'Windows 事件記錄檔常數 (\System32\winevt\logs\application.evtx .h) '
description: Windows 事件記錄檔會定義下列常數
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384613"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="a68d0-103">Windows 事件記錄檔常數</span><span class="sxs-lookup"><span data-stu-id="a68d0-103">Windows Event Log Constants</span></span>

<span data-ttu-id="a68d0-104">Windows 事件記錄檔會定義下列常數：</span><span class="sxs-lookup"><span data-stu-id="a68d0-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="a68d0-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**.EVT \_ VARIANT \_ 類型 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="a68d0-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a68d0-106">0x7f</span><span class="sxs-lookup"><span data-stu-id="a68d0-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="a68d0-107">用來將 variant 類型的陣列位遮罩的位元遮罩，讓您可以判斷 [**.Evt \_ variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) 結構包含的 variant 值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a68d0-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a68d0-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**.EVT \_ VARIANT \_ 類型 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="a68d0-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a68d0-109">128</span><span class="sxs-lookup"><span data-stu-id="a68d0-109">128</span></span>
</dt> <dt>



<span data-ttu-id="a68d0-110">如果變數包含值陣列的指標，而不是值本身，則 [**.Evt \_ VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant)結構的 **類型** 成員會設定此位。</span><span class="sxs-lookup"><span data-stu-id="a68d0-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a68d0-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**.EVT \_ 讀取 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="a68d0-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a68d0-112">0x1</span><span class="sxs-lookup"><span data-stu-id="a68d0-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="a68d0-113">讀取存取控制許可權，允許從事件記錄檔讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="a68d0-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a68d0-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**.EVT \_ 寫入 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="a68d0-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a68d0-115">0x2</span><span class="sxs-lookup"><span data-stu-id="a68d0-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="a68d0-116">寫入存取控制許可權，允許將資訊寫入事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a68d0-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a68d0-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**.EVT \_ 清楚 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="a68d0-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a68d0-118">0x4</span><span class="sxs-lookup"><span data-stu-id="a68d0-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="a68d0-119">清除存取控制許可權，允許從事件記錄檔中清除所有資訊。</span><span class="sxs-lookup"><span data-stu-id="a68d0-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a68d0-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**.EVT \_ 所有 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="a68d0-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a68d0-121">0x7</span><span class="sxs-lookup"><span data-stu-id="a68d0-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="a68d0-122">所有 (讀取、寫入、清除和刪除) 存取控制許可權。</span><span class="sxs-lookup"><span data-stu-id="a68d0-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a68d0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a68d0-123">Requirements</span></span>



| <span data-ttu-id="a68d0-124">需求</span><span class="sxs-lookup"><span data-stu-id="a68d0-124">Requirement</span></span> | <span data-ttu-id="a68d0-125">值</span><span class="sxs-lookup"><span data-stu-id="a68d0-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a68d0-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a68d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a68d0-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a68d0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a68d0-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a68d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a68d0-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a68d0-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a68d0-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a68d0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a68d0-131"><dt>\System32\winevt\logs\application.evtx。h</dt></span><span class="sxs-lookup"><span data-stu-id="a68d0-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





