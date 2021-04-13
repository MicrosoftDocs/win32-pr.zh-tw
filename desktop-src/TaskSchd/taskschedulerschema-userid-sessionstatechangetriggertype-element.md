---
title: UserId (sessionStateChangeTriggerType) 元素
description: 包含終端機伺服器會話的使用者。 當偵測到此使用者的會話狀態變更時，就會啟動工作。
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- UserId 元素工作排程器
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509115"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="d3e90-105">UserId (sessionStateChangeTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="d3e90-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="d3e90-106">包含終端機伺服器會話的使用者。</span><span class="sxs-lookup"><span data-stu-id="d3e90-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="d3e90-107">當偵測到此使用者的會話狀態變更時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="d3e90-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="d3e90-108">**UserId** 元素是由 [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d3e90-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d3e90-109">父元素</span><span class="sxs-lookup"><span data-stu-id="d3e90-109">Parent element</span></span>



| <span data-ttu-id="d3e90-110">元素</span><span class="sxs-lookup"><span data-stu-id="d3e90-110">Element</span></span>                       | <span data-ttu-id="d3e90-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="d3e90-111">Derived from</span></span>                                                                                           | <span data-ttu-id="d3e90-112">Description</span><span class="sxs-lookup"><span data-stu-id="d3e90-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e90-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="d3e90-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="d3e90-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d3e90-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="d3e90-115">指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d3e90-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d3e90-116">備註</span><span class="sxs-lookup"><span data-stu-id="d3e90-116">Remarks</span></span>

<span data-ttu-id="d3e90-117">針對 c + + 開發，請參閱 [**ISessionStateChangeTrigger 的 UserId 屬性**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid)。</span><span class="sxs-lookup"><span data-stu-id="d3e90-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="d3e90-118">如需腳本開發，請參閱 [**SessionStateChangeTrigger。 UserId**](sessionstatechangetrigger-userid.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e90-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e90-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3e90-119">Requirements</span></span>



| <span data-ttu-id="d3e90-120">需求</span><span class="sxs-lookup"><span data-stu-id="d3e90-120">Requirement</span></span> | <span data-ttu-id="d3e90-121">值</span><span class="sxs-lookup"><span data-stu-id="d3e90-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3e90-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3e90-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e90-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3e90-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3e90-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3e90-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e90-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3e90-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





