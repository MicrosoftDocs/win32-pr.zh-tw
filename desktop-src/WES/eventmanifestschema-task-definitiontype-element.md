---
title: task (DefinitionType) 元素
description: 定義您的提供者可以記錄的工作特定事件。 |task (DefinitionType) 元素
ms.assetid: 0e880720-1896-43cf-b702-cabca8ab1430
keywords:
- task 元素 EventLog
topic_type:
- apiref
api_name:
- task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35fe629c17b8ede4064de3fb11d05c8e8c84f202
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998979"
---
# <a name="task-definitiontype-element"></a><span data-ttu-id="cc32c-105">task (DefinitionType) 元素</span><span class="sxs-lookup"><span data-stu-id="cc32c-105">task (DefinitionType) Element</span></span>

<span data-ttu-id="cc32c-106">\[從 Windows 7 版 Windows SDK 隨附的訊息編譯器開始，此專案已無法再使用。\]</span><span class="sxs-lookup"><span data-stu-id="cc32c-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="cc32c-107">定義您的提供者可以記錄的工作特定事件。</span><span class="sxs-lookup"><span data-stu-id="cc32c-107">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:element name="task"
    type="TaskEventDefinitionType"
 />
```

<span data-ttu-id="cc32c-108">**Task** 專案是由 [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="cc32c-108">The **task** element is defined by the [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc32c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc32c-109">Requirements</span></span>



| <span data-ttu-id="cc32c-110">需求</span><span class="sxs-lookup"><span data-stu-id="cc32c-110">Requirement</span></span> | <span data-ttu-id="cc32c-111">值</span><span class="sxs-lookup"><span data-stu-id="cc32c-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc32c-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc32c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cc32c-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc32c-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc32c-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc32c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cc32c-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc32c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc32c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc32c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc32c-117">**父元素**</span><span class="sxs-lookup"><span data-stu-id="cc32c-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="cc32c-118">**事件 (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="cc32c-118">**events (ProviderType)**</span></span>](eventmanifestschema-events-providertype-element.md)
</dt> </dl>

 

 





