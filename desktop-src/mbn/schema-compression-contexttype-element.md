---
description: 指定壓縮是否會用於標頭和資料傳輸的資料連結。
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: 壓縮 (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848113"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="c7bcb-103">壓縮 (coNtextType) 元素</span><span class="sxs-lookup"><span data-stu-id="c7bcb-103">Compression (contextType) Element</span></span>

<span data-ttu-id="c7bcb-104">**壓縮 (coNtextType)** 元素會指定壓縮是否會用於標頭和資料傳輸的資料連結。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="c7bcb-105">這個元素可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="c7bcb-106">值</span><span class="sxs-lookup"><span data-stu-id="c7bcb-106">Value</span></span>     | <span data-ttu-id="c7bcb-107">意義</span><span class="sxs-lookup"><span data-stu-id="c7bcb-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="c7bcb-108">禁用</span><span class="sxs-lookup"><span data-stu-id="c7bcb-108">"ENABLE"</span></span>  | <span data-ttu-id="c7bcb-109">將會使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-109">Compression will be used.</span></span>     |
| <span data-ttu-id="c7bcb-110">停用</span><span class="sxs-lookup"><span data-stu-id="c7bcb-110">"DISABLE"</span></span> | <span data-ttu-id="c7bcb-111">將不會使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="c7bcb-112">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-112">This element is optional.</span></span> <span data-ttu-id="c7bcb-113">如果未指定此元素，行動寬頻系統將不會使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="c7bcb-114">**壓縮** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c7bcb-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bcb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7bcb-115">Requirements</span></span>



| <span data-ttu-id="c7bcb-116">需求</span><span class="sxs-lookup"><span data-stu-id="c7bcb-116">Requirement</span></span> | <span data-ttu-id="c7bcb-117">值</span><span class="sxs-lookup"><span data-stu-id="c7bcb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c7bcb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7bcb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7bcb-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7bcb-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c7bcb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7bcb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7bcb-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7bcb-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c7bcb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7bcb-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7bcb-123">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="c7bcb-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c7bcb-124">**coNtextType**</span><span class="sxs-lookup"><span data-stu-id="c7bcb-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="c7bcb-125">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="c7bcb-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c7bcb-126">**MBNProfile) 內容 (**</span><span class="sxs-lookup"><span data-stu-id="c7bcb-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




