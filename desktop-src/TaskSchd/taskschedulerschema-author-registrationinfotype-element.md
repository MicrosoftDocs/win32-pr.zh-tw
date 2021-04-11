---
title: 編寫 (registrationInfoType) 元素
description: 指定工作的作者。
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Author 元素工作排程器
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934594"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="9589d-104">編寫 (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="9589d-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="9589d-105">指定工作的作者。</span><span class="sxs-lookup"><span data-stu-id="9589d-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="9589d-106">**Author** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="9589d-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9589d-107">父元素</span><span class="sxs-lookup"><span data-stu-id="9589d-107">Parent element</span></span>



| <span data-ttu-id="9589d-108">元素</span><span class="sxs-lookup"><span data-stu-id="9589d-108">Element</span></span>                                                                           | <span data-ttu-id="9589d-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="9589d-109">Derived from</span></span>                                                                         | <span data-ttu-id="9589d-110">Description</span><span class="sxs-lookup"><span data-stu-id="9589d-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9589d-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="9589d-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="9589d-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="9589d-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="9589d-113">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="9589d-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9589d-114">備註</span><span class="sxs-lookup"><span data-stu-id="9589d-114">Remarks</span></span>

<span data-ttu-id="9589d-115">針對開發腳本，工作的作者是使用 [**RegistrationInfo. author**](registrationinfo-author.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="9589d-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="9589d-116">若是 c + + 開發，則會使用 [**IRegistrationInfo：： author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) 屬性來指定工作的作者。</span><span class="sxs-lookup"><span data-stu-id="9589d-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9589d-117">範例</span><span class="sxs-lookup"><span data-stu-id="9589d-117">Examples</span></span>

<span data-ttu-id="9589d-118">下列 XML 定義工作的作者。</span><span class="sxs-lookup"><span data-stu-id="9589d-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="9589d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9589d-119">Requirements</span></span>



| <span data-ttu-id="9589d-120">需求</span><span class="sxs-lookup"><span data-stu-id="9589d-120">Requirement</span></span> | <span data-ttu-id="9589d-121">值</span><span class="sxs-lookup"><span data-stu-id="9589d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9589d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9589d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9589d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9589d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9589d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9589d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9589d-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9589d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9589d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9589d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9589d-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="9589d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9589d-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9589d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





