---
description: 識別要用來建立資料連線的 APN 或撥號字串。
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: AccessString (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974053"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="0626d-103">AccessString (coNtextType) 元素</span><span class="sxs-lookup"><span data-stu-id="0626d-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="0626d-104">**AccessString (coNtextType)** 元素會識別要用來建立資料連線的 APN 或撥號字串。</span><span class="sxs-lookup"><span data-stu-id="0626d-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="0626d-105">這個元素的最大長度可以是100個字元。</span><span class="sxs-lookup"><span data-stu-id="0626d-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="0626d-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="0626d-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0626d-107">**AccessString** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="0626d-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0626d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="0626d-108">Requirements</span></span>



| <span data-ttu-id="0626d-109">需求</span><span class="sxs-lookup"><span data-stu-id="0626d-109">Requirement</span></span> | <span data-ttu-id="0626d-110">值</span><span class="sxs-lookup"><span data-stu-id="0626d-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="0626d-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0626d-111">Minimum supported client</span></span><br/> | <span data-ttu-id="0626d-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0626d-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="0626d-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0626d-113">Minimum supported server</span></span><br/> | <span data-ttu-id="0626d-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="0626d-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="0626d-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0626d-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="0626d-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="0626d-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0626d-117">**coNtextType**</span><span class="sxs-lookup"><span data-stu-id="0626d-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="0626d-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="0626d-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0626d-119">**MBNProfile) 內容 (**</span><span class="sxs-lookup"><span data-stu-id="0626d-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




