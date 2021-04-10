---
title: 執行 (SystemPropertiesType) 元素
description: 包含記錄事件之進程和執行緒的相關資訊。
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- 執行元素 EventLog
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685622"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="5e5c2-104">執行 (SystemPropertiesType) 元素</span><span class="sxs-lookup"><span data-stu-id="5e5c2-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="5e5c2-105">包含記錄事件之進程和執行緒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="5e5c2-106">**執行** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="5e5c2-107">屬性</span><span class="sxs-lookup"><span data-stu-id="5e5c2-107">Attributes</span></span>



| <span data-ttu-id="5e5c2-108">名稱</span><span class="sxs-lookup"><span data-stu-id="5e5c2-108">Name</span></span>          | <span data-ttu-id="5e5c2-109">類型</span><span class="sxs-lookup"><span data-stu-id="5e5c2-109">Type</span></span>         | <span data-ttu-id="5e5c2-110">Description</span><span class="sxs-lookup"><span data-stu-id="5e5c2-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5c2-111">KernelTime</span><span class="sxs-lookup"><span data-stu-id="5e5c2-111">KernelTime</span></span>    | <span data-ttu-id="5e5c2-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e5c2-112">unsignedInt</span></span>  | <span data-ttu-id="5e5c2-113">核心模式指令的已耗用執行時間，以 CPU 時間單位表示。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="5e5c2-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="5e5c2-114">ProcessID</span></span>     | <span data-ttu-id="5e5c2-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e5c2-115">unsignedInt</span></span>  | <span data-ttu-id="5e5c2-116">識別已產生事件的處理序。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="5e5c2-117">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="5e5c2-117">ProcessorID</span></span>   | <span data-ttu-id="5e5c2-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5e5c2-118">unsignedByte</span></span> | <span data-ttu-id="5e5c2-119">處理事件之處理器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="5e5c2-120">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="5e5c2-120">ProcessorTime</span></span> | <span data-ttu-id="5e5c2-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e5c2-121">unsignedInt</span></span>  | <span data-ttu-id="5e5c2-122">針對 ETW 私用會話，使用者模式指示的經過執行時間，以 CPU 滴答為單位。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="5e5c2-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="5e5c2-123">SessionID</span></span>     | <span data-ttu-id="5e5c2-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e5c2-124">unsignedInt</span></span>  | <span data-ttu-id="5e5c2-125">發生事件之終端機伺服器工作階段的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="5e5c2-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="5e5c2-126">ThreadID</span></span>      | <span data-ttu-id="5e5c2-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e5c2-127">unsignedInt</span></span>  | <span data-ttu-id="5e5c2-128">識別已產生事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="5e5c2-129">UserTime</span><span class="sxs-lookup"><span data-stu-id="5e5c2-129">UserTime</span></span>      | <span data-ttu-id="5e5c2-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e5c2-130">unsignedInt</span></span>  | <span data-ttu-id="5e5c2-131">使用者模式指示的經過執行時間，以 CPU 時間單位表示。</span><span class="sxs-lookup"><span data-stu-id="5e5c2-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="5e5c2-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e5c2-132">Requirements</span></span>



| <span data-ttu-id="5e5c2-133">需求</span><span class="sxs-lookup"><span data-stu-id="5e5c2-133">Requirement</span></span> | <span data-ttu-id="5e5c2-134">值</span><span class="sxs-lookup"><span data-stu-id="5e5c2-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e5c2-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e5c2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5c2-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e5c2-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e5c2-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e5c2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5c2-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e5c2-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e5c2-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e5c2-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e5c2-140">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5e5c2-141">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="5e5c2-142">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5e5c2-143">**系統 (的系統事件)**</span><span class="sxs-lookup"><span data-stu-id="5e5c2-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





