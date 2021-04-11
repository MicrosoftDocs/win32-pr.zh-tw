---
title: showMessageType 複雜類型
description: 定義代表顯示訊息方塊之動作的元素。
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- showMessageType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934668"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="4ee74-104">showMessageType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="4ee74-104">showMessageType Complex Type</span></span>

<span data-ttu-id="4ee74-105">定義代表顯示訊息方塊之動作的元素。</span><span class="sxs-lookup"><span data-stu-id="4ee74-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4ee74-106">子元素</span><span class="sxs-lookup"><span data-stu-id="4ee74-106">Child elements</span></span>



| <span data-ttu-id="4ee74-107">元素</span><span class="sxs-lookup"><span data-stu-id="4ee74-107">Element</span></span>                                                            | <span data-ttu-id="4ee74-108">類型</span><span class="sxs-lookup"><span data-stu-id="4ee74-108">Type</span></span>           | <span data-ttu-id="4ee74-109">Description</span><span class="sxs-lookup"><span data-stu-id="4ee74-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="4ee74-110">**本文**</span><span class="sxs-lookup"><span data-stu-id="4ee74-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="4ee74-111">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="4ee74-111">nonEmptyString</span></span> | <span data-ttu-id="4ee74-112">指定要顯示在訊息方塊主體中的文字。</span><span class="sxs-lookup"><span data-stu-id="4ee74-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="4ee74-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="4ee74-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="4ee74-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="4ee74-114">nonEmptyString</span></span> | <span data-ttu-id="4ee74-115">指定訊息方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="4ee74-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="4ee74-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ee74-116">Requirements</span></span>



| <span data-ttu-id="4ee74-117">需求</span><span class="sxs-lookup"><span data-stu-id="4ee74-117">Requirement</span></span> | <span data-ttu-id="4ee74-118">值</span><span class="sxs-lookup"><span data-stu-id="4ee74-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ee74-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ee74-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee74-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee74-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ee74-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ee74-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee74-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee74-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





