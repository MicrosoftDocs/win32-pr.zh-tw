---
title: dayOfMonthType 簡單類型
description: 定義指定月份日期的可能值。
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- dayOfMonthType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508392"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="84fd1-104">dayOfMonthType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="84fd1-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="84fd1-105">定義指定月份日期的可能值。</span><span class="sxs-lookup"><span data-stu-id="84fd1-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="84fd1-106">模式</span><span class="sxs-lookup"><span data-stu-id="84fd1-106">Patterns</span></span>

<span data-ttu-id="84fd1-107">**DayOfMonthType** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="84fd1-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="84fd1-108">指定一個月的第1個到第31天，或一律是當月的最後一天。</span><span class="sxs-lookup"><span data-stu-id="84fd1-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fd1-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="84fd1-109">Requirements</span></span>



| <span data-ttu-id="84fd1-110">需求</span><span class="sxs-lookup"><span data-stu-id="84fd1-110">Requirement</span></span> | <span data-ttu-id="84fd1-111">值</span><span class="sxs-lookup"><span data-stu-id="84fd1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84fd1-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84fd1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="84fd1-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84fd1-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84fd1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="84fd1-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84fd1-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84fd1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fd1-117">工作排程器架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="84fd1-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="84fd1-118">工作排程器</span><span class="sxs-lookup"><span data-stu-id="84fd1-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





