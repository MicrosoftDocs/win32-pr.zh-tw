---
title: Principal (principalType) 元素
description: 指定主體的安全性認證。
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Principal 元素工作排程器
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966293"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="87883-104">Principal (principalType) 元素</span><span class="sxs-lookup"><span data-stu-id="87883-104">Principal (principalType) Element</span></span>

<span data-ttu-id="87883-105">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="87883-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="87883-106">這些認證會定義工作執行所在的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="87883-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="87883-107">**Principal** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="87883-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="87883-108">父元素</span><span class="sxs-lookup"><span data-stu-id="87883-108">Parent element</span></span>



| <span data-ttu-id="87883-109">元素</span><span class="sxs-lookup"><span data-stu-id="87883-109">Element</span></span>                                                               | <span data-ttu-id="87883-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="87883-110">Derived from</span></span>                                                             | <span data-ttu-id="87883-111">Description</span><span class="sxs-lookup"><span data-stu-id="87883-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="87883-112">**主體**</span><span class="sxs-lookup"><span data-stu-id="87883-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="87883-113">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="87883-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="87883-114">指定與工作相關聯的安全性主體。</span><span class="sxs-lookup"><span data-stu-id="87883-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="87883-115">子元素</span><span class="sxs-lookup"><span data-stu-id="87883-115">Child elements</span></span>



| <span data-ttu-id="87883-116">元素</span><span class="sxs-lookup"><span data-stu-id="87883-116">Element</span></span>                                                                      | <span data-ttu-id="87883-117">類型</span><span class="sxs-lookup"><span data-stu-id="87883-117">Type</span></span>                                                          | <span data-ttu-id="87883-118">Description</span><span class="sxs-lookup"><span data-stu-id="87883-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87883-119">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="87883-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="87883-120">**string**</span><span class="sxs-lookup"><span data-stu-id="87883-120">**string**</span></span>                                                    | <span data-ttu-id="87883-121">指定工作排程器 UI 中顯示之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="87883-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="87883-122">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="87883-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="87883-123">**string**</span><span class="sxs-lookup"><span data-stu-id="87883-123">**string**</span></span>                                                    | <span data-ttu-id="87883-124">指定執行與主體相關聯之工作所需之使用者群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="87883-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="87883-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="87883-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="87883-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="87883-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="87883-127">指定執行與主體相關聯之工作所需的安全性登入方法。</span><span class="sxs-lookup"><span data-stu-id="87883-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="87883-128">**UserId**</span><span class="sxs-lookup"><span data-stu-id="87883-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="87883-129">**string**</span><span class="sxs-lookup"><span data-stu-id="87883-129">**string**</span></span>                                                    | <span data-ttu-id="87883-130">指定執行與主體相關聯之工作所需的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="87883-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="87883-131">屬性</span><span class="sxs-lookup"><span data-stu-id="87883-131">Attributes</span></span>



| <span data-ttu-id="87883-132">名稱</span><span class="sxs-lookup"><span data-stu-id="87883-132">Name</span></span> | <span data-ttu-id="87883-133">類型</span><span class="sxs-lookup"><span data-stu-id="87883-133">Type</span></span> | <span data-ttu-id="87883-134">Description</span><span class="sxs-lookup"><span data-stu-id="87883-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="87883-135">識別碼</span><span class="sxs-lookup"><span data-stu-id="87883-135">Id</span></span>   | <span data-ttu-id="87883-136">識別碼</span><span class="sxs-lookup"><span data-stu-id="87883-136">ID</span></span>   | <span data-ttu-id="87883-137">主體定義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="87883-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="87883-138">備註</span><span class="sxs-lookup"><span data-stu-id="87883-138">Remarks</span></span>

<span data-ttu-id="87883-139">針對開發腳本，系統會使用 [**principal**](principal.md) 物件來指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="87883-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="87883-140">針對 c + + 開發，系統會使用 [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) 介面來指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="87883-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="87883-141">上方所列的子專案是由 [**principalType**](taskschedulerschema-principaltype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="87883-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="87883-142">如需這些子項目的排序資訊，請參閱 [**principalType**](taskschedulerschema-principaltype-complextype.md)。</span><span class="sxs-lookup"><span data-stu-id="87883-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="87883-143">範例</span><span class="sxs-lookup"><span data-stu-id="87883-143">Examples</span></span>

<span data-ttu-id="87883-144">下列 XML 會定義具有使用者識別碼的主體。</span><span class="sxs-lookup"><span data-stu-id="87883-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="87883-145">下列 XML 會定義具有群組識別碼的主體。</span><span class="sxs-lookup"><span data-stu-id="87883-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="87883-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="87883-146">Requirements</span></span>



| <span data-ttu-id="87883-147">需求</span><span class="sxs-lookup"><span data-stu-id="87883-147">Requirement</span></span> | <span data-ttu-id="87883-148">值</span><span class="sxs-lookup"><span data-stu-id="87883-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87883-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87883-149">Minimum supported client</span></span><br/> | <span data-ttu-id="87883-150">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87883-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87883-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87883-151">Minimum supported server</span></span><br/> | <span data-ttu-id="87883-152">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87883-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87883-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87883-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87883-154">工作排程器</span><span class="sxs-lookup"><span data-stu-id="87883-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





