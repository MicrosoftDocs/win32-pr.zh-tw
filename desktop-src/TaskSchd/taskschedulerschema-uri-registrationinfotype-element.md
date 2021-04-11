---
title: URI (registrationInfoType) 元素
description: 指定工作的 URI。
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- URI 元素工作排程器
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686552"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="75aa7-104">URI (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="75aa7-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="75aa7-105">指定工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="75aa7-105">Specifies the URI of the task.</span></span> <span data-ttu-id="75aa7-106">這個元素是用來指定已註冊的工作放置於工作資料夾階層中的位置。</span><span class="sxs-lookup"><span data-stu-id="75aa7-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="75aa7-107">**URI** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="75aa7-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="75aa7-108">父元素</span><span class="sxs-lookup"><span data-stu-id="75aa7-108">Parent element</span></span>



| <span data-ttu-id="75aa7-109">元素</span><span class="sxs-lookup"><span data-stu-id="75aa7-109">Element</span></span>                                                                           | <span data-ttu-id="75aa7-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="75aa7-110">Derived from</span></span>                                                                         | <span data-ttu-id="75aa7-111">Description</span><span class="sxs-lookup"><span data-stu-id="75aa7-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75aa7-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="75aa7-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="75aa7-113">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="75aa7-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="75aa7-114">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="75aa7-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="75aa7-115">備註</span><span class="sxs-lookup"><span data-stu-id="75aa7-115">Remarks</span></span>

<span data-ttu-id="75aa7-116">針對開發腳本，工作的 URI 是使用 [**RegistrationInfo**](registrationinfo-uri.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="75aa7-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="75aa7-117">若是 c + + 開發，則會使用 [**IRegistrationInfo：： URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) 屬性來指定工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="75aa7-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="75aa7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="75aa7-118">Requirements</span></span>



| <span data-ttu-id="75aa7-119">需求</span><span class="sxs-lookup"><span data-stu-id="75aa7-119">Requirement</span></span> | <span data-ttu-id="75aa7-120">值</span><span class="sxs-lookup"><span data-stu-id="75aa7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75aa7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75aa7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="75aa7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75aa7-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75aa7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75aa7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="75aa7-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75aa7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75aa7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75aa7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75aa7-126">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="75aa7-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="75aa7-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="75aa7-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





