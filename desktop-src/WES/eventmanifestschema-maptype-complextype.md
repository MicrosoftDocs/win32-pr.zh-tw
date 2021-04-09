---
title: MapType 複雜類型
description: 定義成對名稱/值的清單。
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- MapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685630"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="234ed-104">MapType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="234ed-104">MapType Complex Type</span></span>

<span data-ttu-id="234ed-105">定義成對名稱/值的清單。</span><span class="sxs-lookup"><span data-stu-id="234ed-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="234ed-106">子元素</span><span class="sxs-lookup"><span data-stu-id="234ed-106">Child elements</span></span>



| <span data-ttu-id="234ed-107">元素</span><span class="sxs-lookup"><span data-stu-id="234ed-107">Element</span></span>                                                          | <span data-ttu-id="234ed-108">類型</span><span class="sxs-lookup"><span data-stu-id="234ed-108">Type</span></span>                                                                 | <span data-ttu-id="234ed-109">Description</span><span class="sxs-lookup"><span data-stu-id="234ed-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="234ed-110">**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="234ed-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="234ed-111">**BitMapType**</span><span class="sxs-lookup"><span data-stu-id="234ed-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="234ed-112">定義對應位值和字串值的名稱/值組清單。</span><span class="sxs-lookup"><span data-stu-id="234ed-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="234ed-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="234ed-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="234ed-114">**ValueMapType**</span><span class="sxs-lookup"><span data-stu-id="234ed-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="234ed-115">定義對應整數值和字串值的名稱/值組清單。</span><span class="sxs-lookup"><span data-stu-id="234ed-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="234ed-116">備註</span><span class="sxs-lookup"><span data-stu-id="234ed-116">Remarks</span></span>

<span data-ttu-id="234ed-117">一般而言，您會建立對應，以提供事件資料的列舉字串值。</span><span class="sxs-lookup"><span data-stu-id="234ed-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="234ed-118">範例</span><span class="sxs-lookup"><span data-stu-id="234ed-118">Examples</span></span>

<span data-ttu-id="234ed-119">下列範例顯示如何指定值對應和點陣圖。</span><span class="sxs-lookup"><span data-stu-id="234ed-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="234ed-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="234ed-120">Requirements</span></span>



| <span data-ttu-id="234ed-121">需求</span><span class="sxs-lookup"><span data-stu-id="234ed-121">Requirement</span></span> | <span data-ttu-id="234ed-122">值</span><span class="sxs-lookup"><span data-stu-id="234ed-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="234ed-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="234ed-123">Minimum supported client</span></span><br/> | <span data-ttu-id="234ed-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="234ed-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="234ed-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="234ed-125">Minimum supported server</span></span><br/> | <span data-ttu-id="234ed-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="234ed-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





