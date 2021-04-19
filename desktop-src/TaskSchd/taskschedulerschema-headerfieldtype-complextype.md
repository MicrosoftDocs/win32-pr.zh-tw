---
title: headerFieldType 複雜類型
description: 定義用來在電子郵件訊息中建立標頭欄位的元素。
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- headerFieldType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969572"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="26d05-104">headerFieldType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="26d05-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="26d05-105">定義用來在電子郵件訊息中建立標頭欄位的元素。</span><span class="sxs-lookup"><span data-stu-id="26d05-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="26d05-106">子元素</span><span class="sxs-lookup"><span data-stu-id="26d05-106">Child elements</span></span>



| <span data-ttu-id="26d05-107">元素</span><span class="sxs-lookup"><span data-stu-id="26d05-107">Element</span></span>                                                            | <span data-ttu-id="26d05-108">類型</span><span class="sxs-lookup"><span data-stu-id="26d05-108">Type</span></span>                                                                    | <span data-ttu-id="26d05-109">Description</span><span class="sxs-lookup"><span data-stu-id="26d05-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="26d05-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="26d05-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="26d05-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="26d05-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="26d05-112">在電子郵件訊息中指定標頭欄位的名稱。</span><span class="sxs-lookup"><span data-stu-id="26d05-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="26d05-113">**值**</span><span class="sxs-lookup"><span data-stu-id="26d05-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="26d05-114">**string**</span><span class="sxs-lookup"><span data-stu-id="26d05-114">**string**</span></span>                                                              | <span data-ttu-id="26d05-115">指定電子郵件訊息中標頭欄位的值。</span><span class="sxs-lookup"><span data-stu-id="26d05-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="26d05-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="26d05-116">Requirements</span></span>



| <span data-ttu-id="26d05-117">需求</span><span class="sxs-lookup"><span data-stu-id="26d05-117">Requirement</span></span> | <span data-ttu-id="26d05-118">值</span><span class="sxs-lookup"><span data-stu-id="26d05-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26d05-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26d05-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26d05-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26d05-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26d05-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26d05-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26d05-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26d05-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





