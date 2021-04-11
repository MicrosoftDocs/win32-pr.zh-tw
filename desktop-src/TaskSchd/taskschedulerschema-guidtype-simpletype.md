---
title: 'guidType 簡單類型 (工作排程器) '
description: 定義有效 Guid 的模式。
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- guidType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105372"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="e852e-104">guidType 簡單類型 (工作排程器) </span><span class="sxs-lookup"><span data-stu-id="e852e-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="e852e-105">定義有效 Guid 的模式。</span><span class="sxs-lookup"><span data-stu-id="e852e-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="e852e-106">模式</span><span class="sxs-lookup"><span data-stu-id="e852e-106">Patterns</span></span>

<span data-ttu-id="e852e-107">**GuidType** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="e852e-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="e852e-108">唯一的128位數位。</span><span class="sxs-lookup"><span data-stu-id="e852e-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="e852e-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="e852e-109">Requirements</span></span>



| <span data-ttu-id="e852e-110">需求</span><span class="sxs-lookup"><span data-stu-id="e852e-110">Requirement</span></span> | <span data-ttu-id="e852e-111">值</span><span class="sxs-lookup"><span data-stu-id="e852e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e852e-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e852e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e852e-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e852e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e852e-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e852e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e852e-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e852e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e852e-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e852e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e852e-117">工作排程器架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="e852e-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="e852e-118">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e852e-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





