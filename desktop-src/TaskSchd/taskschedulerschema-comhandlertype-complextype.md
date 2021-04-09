---
title: comHandlerType 複雜類型
description: 定義 ComHandler 元素的子項目和排序資訊。
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- comHandlerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024884"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="3d964-104">comHandlerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="3d964-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="3d964-105">定義 [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="3d964-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3d964-106">子元素</span><span class="sxs-lookup"><span data-stu-id="3d964-106">Child elements</span></span>



| <span data-ttu-id="3d964-107">元素</span><span class="sxs-lookup"><span data-stu-id="3d964-107">Element</span></span>                                                               | <span data-ttu-id="3d964-108">類型</span><span class="sxs-lookup"><span data-stu-id="3d964-108">Type</span></span>                                                         | <span data-ttu-id="3d964-109">Description</span><span class="sxs-lookup"><span data-stu-id="3d964-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="3d964-110">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="3d964-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="3d964-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="3d964-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="3d964-112">指定處理常式類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d964-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="3d964-113">**資料**</span><span class="sxs-lookup"><span data-stu-id="3d964-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="3d964-114">**dataType**</span><span class="sxs-lookup"><span data-stu-id="3d964-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="3d964-115">指定與處理常式相關聯的其他資料。</span><span class="sxs-lookup"><span data-stu-id="3d964-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="3d964-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d964-116">Requirements</span></span>



| <span data-ttu-id="3d964-117">需求</span><span class="sxs-lookup"><span data-stu-id="3d964-117">Requirement</span></span> | <span data-ttu-id="3d964-118">值</span><span class="sxs-lookup"><span data-stu-id="3d964-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3d964-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d964-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d964-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d964-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3d964-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d964-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d964-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d964-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d964-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d964-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d964-124">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="3d964-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3d964-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3d964-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





