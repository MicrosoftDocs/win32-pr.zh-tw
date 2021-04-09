---
title: namedValue 複雜類型
description: 定義與名稱/值配對中的值相關聯的名稱。
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- namedValue 複雜類型工作排程器
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934672"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="5a4e4-104">namedValue 複雜類型</span><span class="sxs-lookup"><span data-stu-id="5a4e4-104">namedValue Complex Type</span></span>

<span data-ttu-id="5a4e4-105">定義與名稱/值配對中的值相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a4e4-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="5a4e4-106">屬性</span><span class="sxs-lookup"><span data-stu-id="5a4e4-106">Attributes</span></span>



| <span data-ttu-id="5a4e4-107">名稱</span><span class="sxs-lookup"><span data-stu-id="5a4e4-107">Name</span></span> | <span data-ttu-id="5a4e4-108">類型</span><span class="sxs-lookup"><span data-stu-id="5a4e4-108">Type</span></span>                                                                    | <span data-ttu-id="5a4e4-109">描述</span><span class="sxs-lookup"><span data-stu-id="5a4e4-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e4-110">NAME</span><span class="sxs-lookup"><span data-stu-id="5a4e4-110">name</span></span> | [<span data-ttu-id="5a4e4-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="5a4e4-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="5a4e4-112">指定與名稱/值配對中的值相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a4e4-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="5a4e4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a4e4-113">Requirements</span></span>



| <span data-ttu-id="5a4e4-114">需求</span><span class="sxs-lookup"><span data-stu-id="5a4e4-114">Requirement</span></span> | <span data-ttu-id="5a4e4-115">值</span><span class="sxs-lookup"><span data-stu-id="5a4e4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a4e4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a4e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a4e4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a4e4-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a4e4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a4e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a4e4-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a4e4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





