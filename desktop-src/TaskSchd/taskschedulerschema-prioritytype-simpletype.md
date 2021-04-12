---
title: priorityType 簡單類型
description: 定義 Priority (settingsType) 元素的最小值和最大值。
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- priorityType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025339"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="1358c-104">priorityType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="1358c-104">priorityType Simple Type</span></span>

<span data-ttu-id="1358c-105">定義 [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) 元素的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="1358c-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="1358c-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="1358c-106">Enumeration values</span></span>

<span data-ttu-id="1358c-107">**PriorityType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="1358c-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="1358c-108">值</span><span class="sxs-lookup"><span data-stu-id="1358c-108">Value</span></span> | <span data-ttu-id="1358c-109">描述</span><span class="sxs-lookup"><span data-stu-id="1358c-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="1358c-110">0</span><span class="sxs-lookup"><span data-stu-id="1358c-110">0</span></span>     | <span data-ttu-id="1358c-111">允許的最小整數。</span><span class="sxs-lookup"><span data-stu-id="1358c-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="1358c-112">10</span><span class="sxs-lookup"><span data-stu-id="1358c-112">10</span></span>    | <span data-ttu-id="1358c-113">允許的最大整數。</span><span class="sxs-lookup"><span data-stu-id="1358c-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1358c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1358c-114">Requirements</span></span>



| <span data-ttu-id="1358c-115">需求</span><span class="sxs-lookup"><span data-stu-id="1358c-115">Requirement</span></span> | <span data-ttu-id="1358c-116">值</span><span class="sxs-lookup"><span data-stu-id="1358c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1358c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1358c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1358c-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1358c-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1358c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1358c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1358c-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1358c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1358c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1358c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1358c-122">工作排程器架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="1358c-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1358c-123">工作排程器</span><span class="sxs-lookup"><span data-stu-id="1358c-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





