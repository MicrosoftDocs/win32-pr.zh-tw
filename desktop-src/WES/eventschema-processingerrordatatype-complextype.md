---
title: ProcessingErrorDataType 複雜類型
description: 定義在轉譯事件的事件資料時所發生的錯誤。
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- ProcessingErrorDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105179"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="0a15d-104">ProcessingErrorDataType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="0a15d-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="0a15d-105">定義在轉譯事件的事件資料時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0a15d-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="0a15d-106">如果事件資料與資訊清單中的事件資料範本定義不相符，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0a15d-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
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

## <a name="child-elements"></a><span data-ttu-id="0a15d-107">子元素</span><span class="sxs-lookup"><span data-stu-id="0a15d-107">Child elements</span></span>



| <span data-ttu-id="0a15d-108">元素</span><span class="sxs-lookup"><span data-stu-id="0a15d-108">Element</span></span>                                                                          | <span data-ttu-id="0a15d-109">類型</span><span class="sxs-lookup"><span data-stu-id="0a15d-109">Type</span></span>        | <span data-ttu-id="0a15d-110">Description</span><span class="sxs-lookup"><span data-stu-id="0a15d-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a15d-111">**DataItemName**</span><span class="sxs-lookup"><span data-stu-id="0a15d-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="0a15d-112">字串</span><span class="sxs-lookup"><span data-stu-id="0a15d-112">string</span></span>      | <span data-ttu-id="0a15d-113">造成錯誤之事件資料項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a15d-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="0a15d-114">**錯誤碼**</span><span class="sxs-lookup"><span data-stu-id="0a15d-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="0a15d-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a15d-115">unsignedInt</span></span> | <span data-ttu-id="0a15d-116">轉譯事件資料時所發生的錯誤錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a15d-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="0a15d-117">**EventPayload**</span><span class="sxs-lookup"><span data-stu-id="0a15d-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="0a15d-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="0a15d-118">hexBinary</span></span>   | <span data-ttu-id="0a15d-119">包含整個事件資料的二進位 blob。</span><span class="sxs-lookup"><span data-stu-id="0a15d-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="0a15d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a15d-120">Requirements</span></span>



| <span data-ttu-id="0a15d-121">需求</span><span class="sxs-lookup"><span data-stu-id="0a15d-121">Requirement</span></span> | <span data-ttu-id="0a15d-122">值</span><span class="sxs-lookup"><span data-stu-id="0a15d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a15d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a15d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0a15d-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a15d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a15d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a15d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0a15d-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a15d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





