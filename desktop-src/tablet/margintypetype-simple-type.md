---
description: 定義包含 Margin 元素之 Type 屬性有效值的型別。
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: MarginTypeType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194788"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="63d32-103">MarginTypeType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="63d32-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="63d32-104">定義包含 [Margin 元素](margin-element.md)之 **type** 屬性有效值的型別。</span><span class="sxs-lookup"><span data-stu-id="63d32-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="63d32-105">模式</span><span class="sxs-lookup"><span data-stu-id="63d32-105">Patterns</span></span>

<span data-ttu-id="63d32-106">**MarginTypeType** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="63d32-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="63d32-107">備註</span><span class="sxs-lookup"><span data-stu-id="63d32-107">Remarks</span></span>

<span data-ttu-id="63d32-108">[Margin 元素](margin-element.md)的 **Type** 屬性有效值為 "Left" 和 "Right"。</span><span class="sxs-lookup"><span data-stu-id="63d32-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="63d32-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="63d32-109">Requirements</span></span>



| <span data-ttu-id="63d32-110">需求</span><span class="sxs-lookup"><span data-stu-id="63d32-110">Requirement</span></span> | <span data-ttu-id="63d32-111">值</span><span class="sxs-lookup"><span data-stu-id="63d32-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="63d32-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63d32-112">Minimum supported client</span></span><br/> | <span data-ttu-id="63d32-113">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63d32-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="63d32-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63d32-114">Minimum supported server</span></span><br/> | <span data-ttu-id="63d32-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="63d32-115">None supported</span></span><br/>                                     |



 

 




