---
title: execType 複雜類型
description: 定義 Exec (actionGroup) 元素的子項目和排序資訊。
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- execType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464597"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="387c9-104">execType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="387c9-104">execType Complex Type</span></span>

<span data-ttu-id="387c9-105">定義 [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="387c9-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="387c9-106">子元素</span><span class="sxs-lookup"><span data-stu-id="387c9-106">Child elements</span></span>



| <span data-ttu-id="387c9-107">元素</span><span class="sxs-lookup"><span data-stu-id="387c9-107">Element</span></span>                                                                           | <span data-ttu-id="387c9-108">類型</span><span class="sxs-lookup"><span data-stu-id="387c9-108">Type</span></span>                                                        | <span data-ttu-id="387c9-109">Description</span><span class="sxs-lookup"><span data-stu-id="387c9-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="387c9-110">**引數**</span><span class="sxs-lookup"><span data-stu-id="387c9-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="387c9-111">**string**</span><span class="sxs-lookup"><span data-stu-id="387c9-111">**string**</span></span>                                                  | <span data-ttu-id="387c9-112">指定與命令列操作相關聯的引數。</span><span class="sxs-lookup"><span data-stu-id="387c9-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="387c9-113">**命令**</span><span class="sxs-lookup"><span data-stu-id="387c9-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="387c9-114">**pathType**</span><span class="sxs-lookup"><span data-stu-id="387c9-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="387c9-115">指定要執行的可執行檔或檔。</span><span class="sxs-lookup"><span data-stu-id="387c9-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="387c9-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="387c9-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="387c9-117">**pathType**</span><span class="sxs-lookup"><span data-stu-id="387c9-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="387c9-118">指定可執行檔或可執行檔所使用的檔案所在的目錄。</span><span class="sxs-lookup"><span data-stu-id="387c9-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="387c9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="387c9-119">Requirements</span></span>



| <span data-ttu-id="387c9-120">需求</span><span class="sxs-lookup"><span data-stu-id="387c9-120">Requirement</span></span> | <span data-ttu-id="387c9-121">值</span><span class="sxs-lookup"><span data-stu-id="387c9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="387c9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="387c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="387c9-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="387c9-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="387c9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="387c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="387c9-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="387c9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="387c9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="387c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387c9-127">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="387c9-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="387c9-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="387c9-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





