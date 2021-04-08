---
title: idleTriggerType 複雜類型
description: 定義 IdleTrigger 元素的基底類型。
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- idleTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97868d5b13f224bc55661b681246be29f3a4a20b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685644"
---
# <a name="idletriggertype-complex-type"></a><span data-ttu-id="df80b-104">idleTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="df80b-104">idleTriggerType Complex Type</span></span>

<span data-ttu-id="df80b-105">定義 [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) 元素的基底類型。</span><span class="sxs-lookup"><span data-stu-id="df80b-105">Defines the base type for the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="df80b-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="df80b-106">Requirements</span></span>



| <span data-ttu-id="df80b-107">需求</span><span class="sxs-lookup"><span data-stu-id="df80b-107">Requirement</span></span> | <span data-ttu-id="df80b-108">值</span><span class="sxs-lookup"><span data-stu-id="df80b-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df80b-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df80b-109">Minimum supported client</span></span><br/> | <span data-ttu-id="df80b-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df80b-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df80b-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df80b-111">Minimum supported server</span></span><br/> | <span data-ttu-id="df80b-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df80b-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df80b-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df80b-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df80b-114">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="df80b-114">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="df80b-115">工作排程器</span><span class="sxs-lookup"><span data-stu-id="df80b-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





