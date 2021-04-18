---
description: 定義包含一或多個計數器值的結構。
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: 結構複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983494"
---
# <a name="struct-complex-type"></a><span data-ttu-id="893a6-103">結構複雜類型</span><span class="sxs-lookup"><span data-stu-id="893a6-103">struct Complex Type</span></span>

<span data-ttu-id="893a6-104">定義包含一或多個計數器值的結構。</span><span class="sxs-lookup"><span data-stu-id="893a6-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="893a6-105">屬性</span><span class="sxs-lookup"><span data-stu-id="893a6-105">Attributes</span></span>



| <span data-ttu-id="893a6-106">名稱</span><span class="sxs-lookup"><span data-stu-id="893a6-106">Name</span></span> | <span data-ttu-id="893a6-107">類型</span><span class="sxs-lookup"><span data-stu-id="893a6-107">Type</span></span>                                                                    | <span data-ttu-id="893a6-108">描述</span><span class="sxs-lookup"><span data-stu-id="893a6-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="893a6-109">NAME</span><span class="sxs-lookup"><span data-stu-id="893a6-109">name</span></span> | [<span data-ttu-id="893a6-110">**男人： CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="893a6-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="893a6-111">結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="893a6-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="893a6-112">類型</span><span class="sxs-lookup"><span data-stu-id="893a6-112">type</span></span> | [<span data-ttu-id="893a6-113">**男人： CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="893a6-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="893a6-114">識別結構的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="893a6-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="893a6-115">[CTRPP](ctrpp.md)工具會使用您可以使用的名稱來建立結構變數。</span><span class="sxs-lookup"><span data-stu-id="893a6-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="893a6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="893a6-116">Requirements</span></span>



| <span data-ttu-id="893a6-117">需求</span><span class="sxs-lookup"><span data-stu-id="893a6-117">Requirement</span></span> | <span data-ttu-id="893a6-118">值</span><span class="sxs-lookup"><span data-stu-id="893a6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="893a6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="893a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="893a6-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="893a6-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="893a6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="893a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="893a6-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="893a6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




