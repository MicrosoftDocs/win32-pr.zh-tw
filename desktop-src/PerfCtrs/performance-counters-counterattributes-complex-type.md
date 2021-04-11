---
description: 定義包含最多五個計數器屬性的清單。
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: counterAttributes 複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944252"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="60e9d-103">counterAttributes 複雜類型</span><span class="sxs-lookup"><span data-stu-id="60e9d-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="60e9d-104">定義包含最多五個計數器屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="60e9d-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="60e9d-105">子元素</span><span class="sxs-lookup"><span data-stu-id="60e9d-105">Child elements</span></span>



| <span data-ttu-id="60e9d-106">元素</span><span class="sxs-lookup"><span data-stu-id="60e9d-106">Element</span></span>              | <span data-ttu-id="60e9d-107">類型</span><span class="sxs-lookup"><span data-stu-id="60e9d-107">Type</span></span>                                                                               | <span data-ttu-id="60e9d-108">Description</span><span class="sxs-lookup"><span data-stu-id="60e9d-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e9d-109">**counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="60e9d-109">**counterAttribute**</span></span> | [<span data-ttu-id="60e9d-110">**男人： counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="60e9d-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="60e9d-111">計數器屬性，指定如何在取用者應用程式中顯示計數器資料。</span><span class="sxs-lookup"><span data-stu-id="60e9d-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="60e9d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="60e9d-112">Requirements</span></span>



| <span data-ttu-id="60e9d-113">需求</span><span class="sxs-lookup"><span data-stu-id="60e9d-113">Requirement</span></span> | <span data-ttu-id="60e9d-114">值</span><span class="sxs-lookup"><span data-stu-id="60e9d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60e9d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60e9d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="60e9d-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60e9d-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60e9d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60e9d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="60e9d-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60e9d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




