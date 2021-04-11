---
title: ProcessTokenSidType (principalType) 元素
description: 指定工作的進程安全性識別 (SID) 類型。
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- ProcessTokenSidType 元素工作排程器
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104633"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="91b5b-104">ProcessTokenSidType (principalType) 元素</span><span class="sxs-lookup"><span data-stu-id="91b5b-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="91b5b-105">指定工作的進程安全性識別 (SID) 類型。</span><span class="sxs-lookup"><span data-stu-id="91b5b-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="91b5b-106">**ProcessTokenSidType** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="91b5b-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="91b5b-107">父元素</span><span class="sxs-lookup"><span data-stu-id="91b5b-107">Parent element</span></span>



| <span data-ttu-id="91b5b-108">元素</span><span class="sxs-lookup"><span data-stu-id="91b5b-108">Element</span></span>                                                                  | <span data-ttu-id="91b5b-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="91b5b-109">Derived from</span></span>                                                           | <span data-ttu-id="91b5b-110">Description</span><span class="sxs-lookup"><span data-stu-id="91b5b-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="91b5b-111">**主要**</span><span class="sxs-lookup"><span data-stu-id="91b5b-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="91b5b-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="91b5b-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="91b5b-113">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="91b5b-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91b5b-114">備註</span><span class="sxs-lookup"><span data-stu-id="91b5b-114">Remarks</span></span>

<span data-ttu-id="91b5b-115">針對 c + + 開發，會使用 [**IPrincipal2：:P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) 屬性來指定進程 SID 類型。</span><span class="sxs-lookup"><span data-stu-id="91b5b-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="91b5b-116">範例</span><span class="sxs-lookup"><span data-stu-id="91b5b-116">Examples</span></span>

<span data-ttu-id="91b5b-117">下列 XML 定義工作的進程 SID 類型。</span><span class="sxs-lookup"><span data-stu-id="91b5b-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="91b5b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="91b5b-118">Requirements</span></span>



| <span data-ttu-id="91b5b-119">需求</span><span class="sxs-lookup"><span data-stu-id="91b5b-119">Requirement</span></span> | <span data-ttu-id="91b5b-120">值</span><span class="sxs-lookup"><span data-stu-id="91b5b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="91b5b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91b5b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91b5b-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91b5b-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="91b5b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91b5b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91b5b-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91b5b-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91b5b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91b5b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b5b-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="91b5b-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





