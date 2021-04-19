---
description: 用來將列舉的文字指派給離散值。
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980868"
---
# <a name="enum"></a><span data-ttu-id="3434c-103">列舉</span><span class="sxs-lookup"><span data-stu-id="3434c-103">enum</span></span>

<span data-ttu-id="3434c-104">用來將列舉的文字指派給離散值。</span><span class="sxs-lookup"><span data-stu-id="3434c-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="3434c-105">這些元素的任意數目可能會存在於 [enumeratedList](./propdesc-schema-enumeratedlist.md)下。</span><span class="sxs-lookup"><span data-stu-id="3434c-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="3434c-106">以程式設計的方式，這些會表示為 IPropertyEnumType 物件，其 [**IPropertyEnumType：： GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) 方法會傳回寵物 \_ DISCRETEVALUE。</span><span class="sxs-lookup"><span data-stu-id="3434c-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="3434c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3434c-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="3434c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3434c-108">Element Information</span></span>



| <span data-ttu-id="3434c-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="3434c-109">Parent Element</span></span>                                         | <span data-ttu-id="3434c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3434c-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="3434c-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3434c-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="3434c-112">無</span><span class="sxs-lookup"><span data-stu-id="3434c-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="3434c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3434c-113">Attributes</span></span>



| <span data-ttu-id="3434c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="3434c-114">Attribute</span></span> | <span data-ttu-id="3434c-115">描述</span><span class="sxs-lookup"><span data-stu-id="3434c-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3434c-116">value</span><span class="sxs-lookup"><span data-stu-id="3434c-116">value</span></span>     | <span data-ttu-id="3434c-117">公用。</span><span class="sxs-lookup"><span data-stu-id="3434c-117">Public.</span></span> <span data-ttu-id="3434c-118">必要。</span><span class="sxs-lookup"><span data-stu-id="3434c-118">Required.</span></span> <span data-ttu-id="3434c-119">要指派列舉文字給的離散值 (字串或數位) 。</span><span class="sxs-lookup"><span data-stu-id="3434c-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="3434c-120">text</span><span class="sxs-lookup"><span data-stu-id="3434c-120">text</span></span>      | <span data-ttu-id="3434c-121">公用。</span><span class="sxs-lookup"><span data-stu-id="3434c-121">Public.</span></span> <span data-ttu-id="3434c-122">必要。</span><span class="sxs-lookup"><span data-stu-id="3434c-122">Required.</span></span> <span data-ttu-id="3434c-123">用來顯示列舉值的文字。</span><span class="sxs-lookup"><span data-stu-id="3434c-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="3434c-124">語法允許直接顯示字串或間接顯示字串參考;使用間接顯示字串，使其可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="3434c-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="3434c-125">助憶鍵</span><span class="sxs-lookup"><span data-stu-id="3434c-125">mnemonics</span></span> | <span data-ttu-id="3434c-126">**Windows 7 和更新版本。**</span><span class="sxs-lookup"><span data-stu-id="3434c-126">**Windows 7 and later.**</span></span> <span data-ttu-id="3434c-127">公用。</span><span class="sxs-lookup"><span data-stu-id="3434c-127">Public.</span></span> <span data-ttu-id="3434c-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3434c-128">Optional.</span></span> <span data-ttu-id="3434c-129">助憶鍵值的清單，可用來參考搜尋查詢中的屬性。</span><span class="sxs-lookup"><span data-stu-id="3434c-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="3434c-130">此清單以 ' \| ' 字元分隔。</span><span class="sxs-lookup"><span data-stu-id="3434c-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
