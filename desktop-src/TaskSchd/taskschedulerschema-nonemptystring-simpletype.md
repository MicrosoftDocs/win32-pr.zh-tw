---
title: nonEmptyStringType 簡單類型
description: 定義用於非空白文字字串的值。
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- nonEmptyString 簡單類型工作排程器
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384909"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="058fc-104">nonEmptyStringType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="058fc-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="058fc-105">定義用於非空白文字字串的值。</span><span class="sxs-lookup"><span data-stu-id="058fc-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="058fc-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="058fc-106">Enumeration values</span></span>

<span data-ttu-id="058fc-107">**NonEmptyString** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="058fc-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="058fc-108">值</span><span class="sxs-lookup"><span data-stu-id="058fc-108">Value</span></span> | <span data-ttu-id="058fc-109">描述</span><span class="sxs-lookup"><span data-stu-id="058fc-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="058fc-110">1</span><span class="sxs-lookup"><span data-stu-id="058fc-110">1</span></span>     | <span data-ttu-id="058fc-111">字串至少包含一個字元。</span><span class="sxs-lookup"><span data-stu-id="058fc-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="058fc-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="058fc-112">Requirements</span></span>



| <span data-ttu-id="058fc-113">需求</span><span class="sxs-lookup"><span data-stu-id="058fc-113">Requirement</span></span> | <span data-ttu-id="058fc-114">值</span><span class="sxs-lookup"><span data-stu-id="058fc-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="058fc-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="058fc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="058fc-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="058fc-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="058fc-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="058fc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="058fc-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="058fc-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





