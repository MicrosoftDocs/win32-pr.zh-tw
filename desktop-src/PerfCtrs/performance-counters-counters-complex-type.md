---
description: 定義檢測資訊清單的區段，以識別提供者以及它們所提供的計數器。
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: 計數器複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944251"
---
# <a name="counters-complex-type"></a><span data-ttu-id="75dbe-103">計數器複雜類型</span><span class="sxs-lookup"><span data-stu-id="75dbe-103">counters Complex Type</span></span>

<span data-ttu-id="75dbe-104">定義檢測資訊清單的區段，以識別提供者以及它們所提供的計數器。</span><span class="sxs-lookup"><span data-stu-id="75dbe-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="75dbe-105">子元素</span><span class="sxs-lookup"><span data-stu-id="75dbe-105">Child elements</span></span>



| <span data-ttu-id="75dbe-106">元素</span><span class="sxs-lookup"><span data-stu-id="75dbe-106">Element</span></span>      | <span data-ttu-id="75dbe-107">類型</span><span class="sxs-lookup"><span data-stu-id="75dbe-107">Type</span></span>                                                               | <span data-ttu-id="75dbe-108">Description</span><span class="sxs-lookup"><span data-stu-id="75dbe-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="75dbe-109">**供應商**</span><span class="sxs-lookup"><span data-stu-id="75dbe-109">**provider**</span></span> | [<span data-ttu-id="75dbe-110">**男人：提供者**</span><span class="sxs-lookup"><span data-stu-id="75dbe-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="75dbe-111">識別提供計數器的提供者。</span><span class="sxs-lookup"><span data-stu-id="75dbe-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="75dbe-112">屬性</span><span class="sxs-lookup"><span data-stu-id="75dbe-112">Attributes</span></span>



| <span data-ttu-id="75dbe-113">名稱</span><span class="sxs-lookup"><span data-stu-id="75dbe-113">Name</span></span>          | <span data-ttu-id="75dbe-114">類型</span><span class="sxs-lookup"><span data-stu-id="75dbe-114">Type</span></span> | <span data-ttu-id="75dbe-115">Description</span><span class="sxs-lookup"><span data-stu-id="75dbe-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="75dbe-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="75dbe-116">schemaVersion</span></span> |      | <span data-ttu-id="75dbe-117">用來寫入資訊清單的架構版本。</span><span class="sxs-lookup"><span data-stu-id="75dbe-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="75dbe-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="75dbe-118">Requirements</span></span>



| <span data-ttu-id="75dbe-119">需求</span><span class="sxs-lookup"><span data-stu-id="75dbe-119">Requirement</span></span> | <span data-ttu-id="75dbe-120">值</span><span class="sxs-lookup"><span data-stu-id="75dbe-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75dbe-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75dbe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="75dbe-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75dbe-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75dbe-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75dbe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="75dbe-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75dbe-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75dbe-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75dbe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75dbe-126">**儀錶**</span><span class="sxs-lookup"><span data-stu-id="75dbe-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

