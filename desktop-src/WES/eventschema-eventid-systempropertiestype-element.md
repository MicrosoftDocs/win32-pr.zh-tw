---
title: EventID (SystemPropertiesType) 元素
description: 提供者用來識別事件的識別碼。
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- EventID 元素 EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464561"
---
# <a name="eventid-systempropertiestype-element"></a><span data-ttu-id="d3fe9-104">EventID (SystemPropertiesType) 元素</span><span class="sxs-lookup"><span data-stu-id="d3fe9-104">EventID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="d3fe9-105">提供者用來識別事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3fe9-105">The identifier that the provider used to identify the event.</span></span>

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d3fe9-106">**EventID** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d3fe9-106">The **EventID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3fe9-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3fe9-107">Requirements</span></span>



| <span data-ttu-id="d3fe9-108">需求</span><span class="sxs-lookup"><span data-stu-id="d3fe9-108">Requirement</span></span> | <span data-ttu-id="d3fe9-109">值</span><span class="sxs-lookup"><span data-stu-id="d3fe9-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3fe9-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3fe9-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d3fe9-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3fe9-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3fe9-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3fe9-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d3fe9-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3fe9-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3fe9-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3fe9-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3fe9-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="d3fe9-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="d3fe9-116">**系統 (的系統事件)**</span><span class="sxs-lookup"><span data-stu-id="d3fe9-116">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





