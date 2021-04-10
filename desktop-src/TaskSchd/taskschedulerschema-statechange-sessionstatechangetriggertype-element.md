---
title: StateChange (sessionStateChangeTriggerType) 元素
description: 包含會觸發工作啟動的終端機伺服器會話變更類型。
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- StateChange 元素工作排程器
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106349"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a><span data-ttu-id="5198d-104">StateChange (sessionStateChangeTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="5198d-104">StateChange (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="5198d-105">包含會觸發工作啟動的終端機伺服器會話變更類型。</span><span class="sxs-lookup"><span data-stu-id="5198d-105">Contains the kind of Terminal Server session change that would trigger a task launch.</span></span>

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

<span data-ttu-id="5198d-106">**StateChange** 元素是由 [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="5198d-106">The **StateChange** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5198d-107">父元素</span><span class="sxs-lookup"><span data-stu-id="5198d-107">Parent element</span></span>



| <span data-ttu-id="5198d-108">元素</span><span class="sxs-lookup"><span data-stu-id="5198d-108">Element</span></span>                       | <span data-ttu-id="5198d-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="5198d-109">Derived from</span></span>                                                                                           | <span data-ttu-id="5198d-110">Description</span><span class="sxs-lookup"><span data-stu-id="5198d-110">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5198d-111">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="5198d-111">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="5198d-112">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5198d-112">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="5198d-113">指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5198d-113">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5198d-114">備註</span><span class="sxs-lookup"><span data-stu-id="5198d-114">Remarks</span></span>

<span data-ttu-id="5198d-115">針對 c + + 開發，請參閱 [**ISessionStateChangeTrigger 的 StateChange 屬性**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange)。</span><span class="sxs-lookup"><span data-stu-id="5198d-115">For C++ development, see [**StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span></span>

<span data-ttu-id="5198d-116">如需腳本開發，請參閱 [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md)。</span><span class="sxs-lookup"><span data-stu-id="5198d-116">For script development, see [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5198d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5198d-117">Requirements</span></span>



| <span data-ttu-id="5198d-118">需求</span><span class="sxs-lookup"><span data-stu-id="5198d-118">Requirement</span></span> | <span data-ttu-id="5198d-119">值</span><span class="sxs-lookup"><span data-stu-id="5198d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5198d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5198d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5198d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5198d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5198d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5198d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5198d-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5198d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





