---
title: weekType 簡單類型
description: 定義可以在 Week 元素中使用的值。
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- weekType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094227"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="7a6ca-104">weekType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="7a6ca-104">weekType Simple Type</span></span>

<span data-ttu-id="7a6ca-105">定義可以在 [**Week**](taskschedulerschema-week-weekstype-element.md) 元素中使用的值。</span><span class="sxs-lookup"><span data-stu-id="7a6ca-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="7a6ca-106">模式</span><span class="sxs-lookup"><span data-stu-id="7a6ca-106">Patterns</span></span>

<span data-ttu-id="7a6ca-107">**WeekType** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="7a6ca-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="7a6ca-108">指定月中第四周的第一個 (1-4) 或一律是當月的最後一周。</span><span class="sxs-lookup"><span data-stu-id="7a6ca-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a6ca-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a6ca-109">Requirements</span></span>



| <span data-ttu-id="7a6ca-110">需求</span><span class="sxs-lookup"><span data-stu-id="7a6ca-110">Requirement</span></span> | <span data-ttu-id="7a6ca-111">值</span><span class="sxs-lookup"><span data-stu-id="7a6ca-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a6ca-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a6ca-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7a6ca-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a6ca-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a6ca-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a6ca-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7a6ca-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a6ca-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a6ca-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a6ca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6ca-117">工作排程器架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="7a6ca-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7a6ca-118">工作排程器</span><span class="sxs-lookup"><span data-stu-id="7a6ca-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





