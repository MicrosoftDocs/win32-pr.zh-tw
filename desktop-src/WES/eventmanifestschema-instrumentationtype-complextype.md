---
title: Instrumentationtype.event 複雜類型
description: 定義資訊清單之檢測區段的內容。
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Instrumentationtype.event 複雜類型 EventLog
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968596"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="65908-104">Instrumentationtype.event 複雜類型</span><span class="sxs-lookup"><span data-stu-id="65908-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="65908-105">定義資訊清單之檢測區段的內容。</span><span class="sxs-lookup"><span data-stu-id="65908-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="65908-106">子元素</span><span class="sxs-lookup"><span data-stu-id="65908-106">Child elements</span></span>



| <span data-ttu-id="65908-107">元素</span><span class="sxs-lookup"><span data-stu-id="65908-107">Element</span></span>                                                                  | <span data-ttu-id="65908-108">類型</span><span class="sxs-lookup"><span data-stu-id="65908-108">Type</span></span>                                                             | <span data-ttu-id="65908-109">Description</span><span class="sxs-lookup"><span data-stu-id="65908-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="65908-110">**事件**</span><span class="sxs-lookup"><span data-stu-id="65908-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="65908-111">**EventsType**</span><span class="sxs-lookup"><span data-stu-id="65908-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="65908-112">包含資訊清單所定義之提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="65908-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="65908-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="65908-113">Requirements</span></span>



| <span data-ttu-id="65908-114">需求</span><span class="sxs-lookup"><span data-stu-id="65908-114">Requirement</span></span> | <span data-ttu-id="65908-115">值</span><span class="sxs-lookup"><span data-stu-id="65908-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65908-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65908-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65908-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65908-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65908-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65908-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65908-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65908-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





