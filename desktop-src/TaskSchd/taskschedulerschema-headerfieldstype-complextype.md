---
title: headerFieldsType 複雜類型
description: 定義專案，以指定電子郵件頭的欄位。
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- headerFieldsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464805"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="52d3d-104">headerFieldsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="52d3d-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="52d3d-105">定義專案，以指定電子郵件頭的欄位。</span><span class="sxs-lookup"><span data-stu-id="52d3d-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="52d3d-106">子元素</span><span class="sxs-lookup"><span data-stu-id="52d3d-106">Child elements</span></span>



| <span data-ttu-id="52d3d-107">元素</span><span class="sxs-lookup"><span data-stu-id="52d3d-107">Element</span></span>                                                                         | <span data-ttu-id="52d3d-108">類型</span><span class="sxs-lookup"><span data-stu-id="52d3d-108">Type</span></span>                                                                       | <span data-ttu-id="52d3d-109">Description</span><span class="sxs-lookup"><span data-stu-id="52d3d-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="52d3d-110">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="52d3d-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="52d3d-111">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="52d3d-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="52d3d-112">指定電子郵件標題中的欄位。</span><span class="sxs-lookup"><span data-stu-id="52d3d-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="52d3d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="52d3d-113">Requirements</span></span>



| <span data-ttu-id="52d3d-114">需求</span><span class="sxs-lookup"><span data-stu-id="52d3d-114">Requirement</span></span> | <span data-ttu-id="52d3d-115">值</span><span class="sxs-lookup"><span data-stu-id="52d3d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52d3d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52d3d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52d3d-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52d3d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52d3d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52d3d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52d3d-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52d3d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





