---
title: 版本 (registrationInfoType) 元素
description: 指定工作的版本號碼。
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Version 元素工作排程器
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967523"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="6e073-104">版本 (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="6e073-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="6e073-105">指定工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6e073-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="6e073-106">**Version** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="6e073-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6e073-107">父元素</span><span class="sxs-lookup"><span data-stu-id="6e073-107">Parent element</span></span>



| <span data-ttu-id="6e073-108">元素</span><span class="sxs-lookup"><span data-stu-id="6e073-108">Element</span></span>                                                                           | <span data-ttu-id="6e073-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="6e073-109">Derived from</span></span>                                                                         | <span data-ttu-id="6e073-110">Description</span><span class="sxs-lookup"><span data-stu-id="6e073-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e073-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="6e073-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="6e073-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="6e073-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="6e073-113">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="6e073-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6e073-114">備註</span><span class="sxs-lookup"><span data-stu-id="6e073-114">Remarks</span></span>

<span data-ttu-id="6e073-115">針對開發腳本，會使用 [**RegistrationInfo**](registrationinfo-version.md) 屬性來指定工作的版本。</span><span class="sxs-lookup"><span data-stu-id="6e073-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="6e073-116">針對 c + + 開發，使用 [**IRegistrationInfo：： version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) 屬性指定工作的版本。</span><span class="sxs-lookup"><span data-stu-id="6e073-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="6e073-117">範例</span><span class="sxs-lookup"><span data-stu-id="6e073-117">Examples</span></span>

<span data-ttu-id="6e073-118">下列 XML 會定義工作的版本。</span><span class="sxs-lookup"><span data-stu-id="6e073-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="6e073-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e073-119">Requirements</span></span>



| <span data-ttu-id="6e073-120">需求</span><span class="sxs-lookup"><span data-stu-id="6e073-120">Requirement</span></span> | <span data-ttu-id="6e073-121">值</span><span class="sxs-lookup"><span data-stu-id="6e073-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e073-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e073-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6e073-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e073-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e073-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e073-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6e073-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e073-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e073-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e073-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e073-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="6e073-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6e073-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6e073-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





