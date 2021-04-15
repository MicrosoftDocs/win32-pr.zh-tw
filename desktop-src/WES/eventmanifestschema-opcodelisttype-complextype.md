---
title: OpcodeListType 複雜類型
description: 定義用來識別應用程式元件之作業的操作碼清單。
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- OpcodeListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465181"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="3e7b6-104">OpcodeListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="3e7b6-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="3e7b6-105">定義用來識別應用程式元件之作業的操作碼清單。</span><span class="sxs-lookup"><span data-stu-id="3e7b6-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3e7b6-106">子元素</span><span class="sxs-lookup"><span data-stu-id="3e7b6-106">Child elements</span></span>



| <span data-ttu-id="3e7b6-107">元素</span><span class="sxs-lookup"><span data-stu-id="3e7b6-107">Element</span></span>                                                             | <span data-ttu-id="3e7b6-108">類型</span><span class="sxs-lookup"><span data-stu-id="3e7b6-108">Type</span></span>                                                             | <span data-ttu-id="3e7b6-109">Description</span><span class="sxs-lookup"><span data-stu-id="3e7b6-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="3e7b6-110">**opcode**</span><span class="sxs-lookup"><span data-stu-id="3e7b6-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="3e7b6-111">**OpcodeType**</span><span class="sxs-lookup"><span data-stu-id="3e7b6-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="3e7b6-112">定義應用程式元件內的作業。</span><span class="sxs-lookup"><span data-stu-id="3e7b6-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3e7b6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e7b6-113">Requirements</span></span>



| <span data-ttu-id="3e7b6-114">需求</span><span class="sxs-lookup"><span data-stu-id="3e7b6-114">Requirement</span></span> | <span data-ttu-id="3e7b6-115">值</span><span class="sxs-lookup"><span data-stu-id="3e7b6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e7b6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e7b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7b6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e7b6-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3e7b6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e7b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7b6-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e7b6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





