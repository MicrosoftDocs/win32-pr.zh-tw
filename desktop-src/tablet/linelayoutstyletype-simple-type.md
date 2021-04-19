---
description: 定義 LineLayout 元素之 Style 屬性的有效值。
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: LineLayoutStyleType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994551"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="cbf29-103">LineLayoutStyleType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="cbf29-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="cbf29-104">定義 [LineLayout 元素](linelayout-element.md)之 **Style** 屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="cbf29-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="cbf29-105">模式</span><span class="sxs-lookup"><span data-stu-id="cbf29-105">Patterns</span></span>

<span data-ttu-id="cbf29-106">**LineLayoutStyleType** 簡單類型是以下列模式限制的字串：</span><span class="sxs-lookup"><span data-stu-id="cbf29-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="cbf29-107">備註</span><span class="sxs-lookup"><span data-stu-id="cbf29-107">Remarks</span></span>

<span data-ttu-id="cbf29-108">[LineLayout 元素](linelayout-element.md)的 **Style** 屬性有效值為：</span><span class="sxs-lookup"><span data-stu-id="cbf29-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="cbf29-109">無</span><span class="sxs-lookup"><span data-stu-id="cbf29-109">None</span></span>
-   <span data-ttu-id="cbf29-110">實線</span><span class="sxs-lookup"><span data-stu-id="cbf29-110">Solid</span></span>
-   <span data-ttu-id="cbf29-111">虛線</span><span class="sxs-lookup"><span data-stu-id="cbf29-111">Dash</span></span>
-   <span data-ttu-id="cbf29-112">點</span><span class="sxs-lookup"><span data-stu-id="cbf29-112">Dot</span></span>
-   <span data-ttu-id="cbf29-113">DashDot</span><span class="sxs-lookup"><span data-stu-id="cbf29-113">DashDot</span></span>
-   <span data-ttu-id="cbf29-114">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="cbf29-114">DashDotDot</span></span>
-   <span data-ttu-id="cbf29-115">Double</span><span class="sxs-lookup"><span data-stu-id="cbf29-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf29-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbf29-116">Requirements</span></span>



| <span data-ttu-id="cbf29-117">需求</span><span class="sxs-lookup"><span data-stu-id="cbf29-117">Requirement</span></span> | <span data-ttu-id="cbf29-118">值</span><span class="sxs-lookup"><span data-stu-id="cbf29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cbf29-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbf29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf29-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbf29-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cbf29-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbf29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf29-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="cbf29-122">None supported</span></span><br/>                                     |



 

 




