---
title: actionsType 複雜類型
description: 定義 Actions 元素的子項目和屬性。
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- actionsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385005"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="49ef8-104">actionsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="49ef8-104">actionsType Complex Type</span></span>

<span data-ttu-id="49ef8-105">定義 [**Actions**](taskschedulerschema-actions-tasktype-element.md) 元素的子項目和屬性。</span><span class="sxs-lookup"><span data-stu-id="49ef8-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="49ef8-106">屬性</span><span class="sxs-lookup"><span data-stu-id="49ef8-106">Attributes</span></span>



| <span data-ttu-id="49ef8-107">名稱</span><span class="sxs-lookup"><span data-stu-id="49ef8-107">Name</span></span>    | <span data-ttu-id="49ef8-108">類型</span><span class="sxs-lookup"><span data-stu-id="49ef8-108">Type</span></span>  | <span data-ttu-id="49ef8-109">描述</span><span class="sxs-lookup"><span data-stu-id="49ef8-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ef8-110">Context</span><span class="sxs-lookup"><span data-stu-id="49ef8-110">Context</span></span> | <span data-ttu-id="49ef8-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="49ef8-111">IDREF</span></span> | <span data-ttu-id="49ef8-112">用來做為工作動作之安全性內容之所使用的主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="49ef8-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="49ef8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="49ef8-113">Requirements</span></span>



| <span data-ttu-id="49ef8-114">需求</span><span class="sxs-lookup"><span data-stu-id="49ef8-114">Requirement</span></span> | <span data-ttu-id="49ef8-115">值</span><span class="sxs-lookup"><span data-stu-id="49ef8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49ef8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49ef8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49ef8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49ef8-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49ef8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49ef8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49ef8-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49ef8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49ef8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49ef8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ef8-121">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="49ef8-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="49ef8-122">工作排程器</span><span class="sxs-lookup"><span data-stu-id="49ef8-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





