---
title: DisplayName (principalType) 元素
description: 指定工作排程器 UI 中顯示之主體的名稱。
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- DisplayName 元素工作排程器
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509446"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="b76ee-104">DisplayName (principalType) 元素</span><span class="sxs-lookup"><span data-stu-id="b76ee-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="b76ee-105">指定工作排程器 UI 中顯示之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="b76ee-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="b76ee-106">**DisplayName** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="b76ee-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b76ee-107">父元素</span><span class="sxs-lookup"><span data-stu-id="b76ee-107">Parent element</span></span>



| <span data-ttu-id="b76ee-108">元素</span><span class="sxs-lookup"><span data-stu-id="b76ee-108">Element</span></span>                                                                  | <span data-ttu-id="b76ee-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="b76ee-109">Derived from</span></span>                                                           | <span data-ttu-id="b76ee-110">Description</span><span class="sxs-lookup"><span data-stu-id="b76ee-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b76ee-111">**主要**</span><span class="sxs-lookup"><span data-stu-id="b76ee-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="b76ee-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="b76ee-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="b76ee-113">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="b76ee-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b76ee-114">備註</span><span class="sxs-lookup"><span data-stu-id="b76ee-114">Remarks</span></span>

<span data-ttu-id="b76ee-115">針對腳本開發，主體的顯示名稱是使用 [**principal. DisplayName**](principal-displayname.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="b76ee-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="b76ee-116">針對 c + + 開發，主體的顯示名稱是使用 [**IPrincipal：:D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="b76ee-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b76ee-117">範例</span><span class="sxs-lookup"><span data-stu-id="b76ee-117">Examples</span></span>

<span data-ttu-id="b76ee-118">下列 XML 會使用群組識別碼和顯示名稱來定義。</span><span class="sxs-lookup"><span data-stu-id="b76ee-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="b76ee-119">下列 XML 會使用使用者識別碼和顯示名稱來定義主體。</span><span class="sxs-lookup"><span data-stu-id="b76ee-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="b76ee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b76ee-120">Requirements</span></span>



| <span data-ttu-id="b76ee-121">需求</span><span class="sxs-lookup"><span data-stu-id="b76ee-121">Requirement</span></span> | <span data-ttu-id="b76ee-122">值</span><span class="sxs-lookup"><span data-stu-id="b76ee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b76ee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b76ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b76ee-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b76ee-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b76ee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b76ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b76ee-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b76ee-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b76ee-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b76ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b76ee-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b76ee-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





