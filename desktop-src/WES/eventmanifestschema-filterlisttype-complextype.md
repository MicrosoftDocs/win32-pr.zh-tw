---
title: FilterListType 複雜類型
description: 定義 ETW 控制器可傳遞給提供者的篩選清單，以進一步限制它所寫入的事件。
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- FilterListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317463"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="579df-104">FilterListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="579df-104">FilterListType Complex Type</span></span>

<span data-ttu-id="579df-105">定義 ETW 控制器可傳遞給提供者的篩選清單，以進一步限制它所寫入的事件。</span><span class="sxs-lookup"><span data-stu-id="579df-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="579df-106">子元素</span><span class="sxs-lookup"><span data-stu-id="579df-106">Child elements</span></span>



| <span data-ttu-id="579df-107">元素</span><span class="sxs-lookup"><span data-stu-id="579df-107">Element</span></span>    | <span data-ttu-id="579df-108">類型</span><span class="sxs-lookup"><span data-stu-id="579df-108">Type</span></span>                                                             | <span data-ttu-id="579df-109">Description</span><span class="sxs-lookup"><span data-stu-id="579df-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="579df-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="579df-110">**filter**</span></span> | [<span data-ttu-id="579df-111">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="579df-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="579df-112">篩選準則的清單。</span><span class="sxs-lookup"><span data-stu-id="579df-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="579df-113">備註</span><span class="sxs-lookup"><span data-stu-id="579df-113">Remarks</span></span>

<span data-ttu-id="579df-114">ETW 控制器是一種應用程式，可呼叫 [**StartTrace**](/windows/desktop/ETW/starttrace) 函式來建立 ETW 會話。</span><span class="sxs-lookup"><span data-stu-id="579df-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="579df-115">如需詳細資訊，請參閱 [控制事件追蹤會話](/windows/desktop/ETW/controlling-event-tracing-sessions)。</span><span class="sxs-lookup"><span data-stu-id="579df-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="579df-116">控制器可以使用 [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) 函式來列舉您所定義的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="579df-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="579df-117">然後，控制器會在呼叫 [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) 函式來啟用您的提供者時，傳遞一或多個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="579df-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="579df-118">您的提供者會在 [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) 回呼函式中接收篩選，以及其餘的 enable 參數。</span><span class="sxs-lookup"><span data-stu-id="579df-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="579df-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="579df-119">Requirements</span></span>



| <span data-ttu-id="579df-120">需求</span><span class="sxs-lookup"><span data-stu-id="579df-120">Requirement</span></span> | <span data-ttu-id="579df-121">值</span><span class="sxs-lookup"><span data-stu-id="579df-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="579df-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="579df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="579df-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="579df-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="579df-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="579df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="579df-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="579df-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

