---
title: opcode (OpcodeListType) 元素
description: 包含識別活動的數值，或在應用程式引發事件 (（例如初始化或關閉) ）時所執行之活動內的某個點。
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- opcode 元素 EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106026"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="5f506-104">opcode (OpcodeListType) 元素</span><span class="sxs-lookup"><span data-stu-id="5f506-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="5f506-105">包含識別活動的數值，或在應用程式引發事件 (（例如初始化或關閉) ）時所執行之活動內的某個點。</span><span class="sxs-lookup"><span data-stu-id="5f506-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="5f506-106">**Opcode** 元素是由 [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="5f506-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f506-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f506-107">Requirements</span></span>



| <span data-ttu-id="5f506-108">需求</span><span class="sxs-lookup"><span data-stu-id="5f506-108">Requirement</span></span> | <span data-ttu-id="5f506-109">值</span><span class="sxs-lookup"><span data-stu-id="5f506-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f506-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f506-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5f506-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f506-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f506-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f506-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5f506-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f506-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f506-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f506-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f506-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="5f506-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="5f506-116">**TaskType)  (碼**</span><span class="sxs-lookup"><span data-stu-id="5f506-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="5f506-117">**ProviderType)  (碼**</span><span class="sxs-lookup"><span data-stu-id="5f506-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="5f506-118">**MetadataType)  (碼**</span><span class="sxs-lookup"><span data-stu-id="5f506-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





