---
title: 延遲 (sessionStateChangeTriggerType) 元素
description: 包含值，指出當偵測到終端機伺服器會話狀態變更時，工作開始時間的延遲長度。
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Delay 元素工作排程器
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106379"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="7fab1-104">延遲 (sessionStateChangeTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="7fab1-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="7fab1-105">包含值，指出當偵測到終端機伺服器會話狀態變更時，工作開始時間的延遲長度。</span><span class="sxs-lookup"><span data-stu-id="7fab1-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="7fab1-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="7fab1-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="7fab1-107">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="7fab1-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="7fab1-108">**Delay** 元素是由 [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="7fab1-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7fab1-109">父元素</span><span class="sxs-lookup"><span data-stu-id="7fab1-109">Parent element</span></span>



| <span data-ttu-id="7fab1-110">元素</span><span class="sxs-lookup"><span data-stu-id="7fab1-110">Element</span></span>                       | <span data-ttu-id="7fab1-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="7fab1-111">Derived from</span></span>                                                                                           | <span data-ttu-id="7fab1-112">Description</span><span class="sxs-lookup"><span data-stu-id="7fab1-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fab1-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="7fab1-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="7fab1-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="7fab1-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="7fab1-115">指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7fab1-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="7fab1-116">備註</span><span class="sxs-lookup"><span data-stu-id="7fab1-116">Remarks</span></span>

<span data-ttu-id="7fab1-117">針對開發腳本，會使用 [**SessionStateChangeTrigger**](sessionstatechangetrigger-delay.md) 屬性來指定會話狀態變更觸發程式延遲。</span><span class="sxs-lookup"><span data-stu-id="7fab1-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="7fab1-118">針對 c + + 開發，會使用 [**ISessionStateChangeTrigger 的 delay 屬性**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay)指定會話狀態變更觸發程式延遲。</span><span class="sxs-lookup"><span data-stu-id="7fab1-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fab1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fab1-119">Requirements</span></span>



| <span data-ttu-id="7fab1-120">需求</span><span class="sxs-lookup"><span data-stu-id="7fab1-120">Requirement</span></span> | <span data-ttu-id="7fab1-121">值</span><span class="sxs-lookup"><span data-stu-id="7fab1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7fab1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fab1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7fab1-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7fab1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fab1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7fab1-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fab1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





