---
title: XmlType 複雜類型
description: 定義 XML 片段。
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- XmlType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384621"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="05159-104">XmlType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="05159-104">XmlType Complex Type</span></span>

<span data-ttu-id="05159-105">定義 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="05159-105">Defines an XML fragment.</span></span> <span data-ttu-id="05159-106">允許任何架構實例;片段中的最上層節點必須包含命名空間屬性。</span><span class="sxs-lookup"><span data-stu-id="05159-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="05159-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="05159-107">Requirements</span></span>



| <span data-ttu-id="05159-108">需求</span><span class="sxs-lookup"><span data-stu-id="05159-108">Requirement</span></span> | <span data-ttu-id="05159-109">值</span><span class="sxs-lookup"><span data-stu-id="05159-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05159-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05159-110">Minimum supported client</span></span><br/> | <span data-ttu-id="05159-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05159-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05159-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05159-112">Minimum supported server</span></span><br/> | <span data-ttu-id="05159-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05159-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





