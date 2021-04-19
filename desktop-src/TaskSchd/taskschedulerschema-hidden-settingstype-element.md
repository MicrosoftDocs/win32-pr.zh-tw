---
title: 隱藏的 (settingsType) 元素
description: 指定預設情況下，工作將不會顯示在 UI 中。
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Hidden 元素工作排程器
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965952"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="1d821-104">隱藏的 (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="1d821-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="1d821-105">指定預設情況下，工作將不會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="1d821-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="1d821-106">不過，系統管理員可以使用「主要交換器」來覆寫這項設定，讓所有工作都顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="1d821-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="1d821-107">**Hidden** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="1d821-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1d821-108">父元素</span><span class="sxs-lookup"><span data-stu-id="1d821-108">Parent element</span></span>



| <span data-ttu-id="1d821-109">元素</span><span class="sxs-lookup"><span data-stu-id="1d821-109">Element</span></span>                                                           | <span data-ttu-id="1d821-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="1d821-110">Derived from</span></span>                                                         | <span data-ttu-id="1d821-111">Description</span><span class="sxs-lookup"><span data-stu-id="1d821-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="1d821-112">**設定**</span><span class="sxs-lookup"><span data-stu-id="1d821-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1d821-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="1d821-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1d821-114">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="1d821-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1d821-115">備註</span><span class="sxs-lookup"><span data-stu-id="1d821-115">Remarks</span></span>

<span data-ttu-id="1d821-116">針對 c + + 開發，請參閱 [**ITaskSettings 的 Hidden 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden)。</span><span class="sxs-lookup"><span data-stu-id="1d821-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="1d821-117">如需腳本開發，請參閱 [**TaskSettings。**](tasksettings-hidden.md)</span><span class="sxs-lookup"><span data-stu-id="1d821-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d821-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d821-118">Requirements</span></span>



| <span data-ttu-id="1d821-119">需求</span><span class="sxs-lookup"><span data-stu-id="1d821-119">Requirement</span></span> | <span data-ttu-id="1d821-120">值</span><span class="sxs-lookup"><span data-stu-id="1d821-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d821-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d821-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1d821-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d821-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1d821-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d821-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1d821-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d821-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d821-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d821-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d821-126">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="1d821-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





