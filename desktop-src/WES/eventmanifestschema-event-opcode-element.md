---
title: 事件 (opcode) 元素
description: 定義工作特定作業碼的事件。
ms.assetid: 7ca8fff2-ef1a-45c4-b082-e4745330bf0b
keywords:
- 事件元素 EventLog
topic_type:
- apiref
api_name:
- event
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25f7a7f3a92c07895529d6dad59df22a7389735d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976979"
---
# <a name="event-opcode-element"></a><span data-ttu-id="53711-104">事件 (opcode) 元素</span><span class="sxs-lookup"><span data-stu-id="53711-104">event (opcode) Element</span></span>

<span data-ttu-id="53711-105">\[從 Windows 7 版 Windows SDK 隨附的訊息編譯器開始，此專案已無法再使用。\]</span><span class="sxs-lookup"><span data-stu-id="53711-105">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="53711-106">定義工作特定作業碼的事件。</span><span class="sxs-lookup"><span data-stu-id="53711-106">Defines an event for a task-specific opcode.</span></span>

``` syntax
<xs:element name="event"
    type="EventDefinitionType"
 />
```

<span data-ttu-id="53711-107">**事件** 元素由 [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="53711-107">The **event** element is defined by the [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="53711-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="53711-108">Requirements</span></span>



| <span data-ttu-id="53711-109">需求</span><span class="sxs-lookup"><span data-stu-id="53711-109">Requirement</span></span> | <span data-ttu-id="53711-110">值</span><span class="sxs-lookup"><span data-stu-id="53711-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53711-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53711-111">Minimum supported client</span></span><br/> | <span data-ttu-id="53711-112">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53711-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53711-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53711-113">Minimum supported server</span></span><br/> | <span data-ttu-id="53711-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53711-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53711-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53711-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="53711-116">**父元素**</span><span class="sxs-lookup"><span data-stu-id="53711-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="53711-117">**opcode (TaskEventDefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="53711-117">**opcode (TaskEventDefinitionType)**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)
</dt> </dl>

 

 





