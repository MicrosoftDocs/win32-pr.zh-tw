---
title: logonType 簡單類型
description: 定義 LogonType 元素的可能值。
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- logonType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105215"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="5b407-104">logonType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="5b407-104">logonType Simple Type</span></span>

<span data-ttu-id="5b407-105">定義 [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) 元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="5b407-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="5b407-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="5b407-106">Enumeration values</span></span>

<span data-ttu-id="5b407-107">**LogonType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="5b407-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="5b407-108">值</span><span class="sxs-lookup"><span data-stu-id="5b407-108">Value</span></span>                      | <span data-ttu-id="5b407-109">描述</span><span class="sxs-lookup"><span data-stu-id="5b407-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b407-110">S4U</span><span class="sxs-lookup"><span data-stu-id="5b407-110">S4U</span></span>                        | <span data-ttu-id="5b407-111">使用者必須使用服務登入使用者 (S4U) 登入。</span><span class="sxs-lookup"><span data-stu-id="5b407-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="5b407-112">使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。</span><span class="sxs-lookup"><span data-stu-id="5b407-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="5b407-113">密碼</span><span class="sxs-lookup"><span data-stu-id="5b407-113">Password</span></span>                   | <span data-ttu-id="5b407-114">使用者必須使用密碼登入。</span><span class="sxs-lookup"><span data-stu-id="5b407-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5b407-115">InteractiveToken</span><span class="sxs-lookup"><span data-stu-id="5b407-115">InteractiveToken</span></span>           | <span data-ttu-id="5b407-116">使用者必須已經登入。</span><span class="sxs-lookup"><span data-stu-id="5b407-116">User must already be logged on.</span></span> <span data-ttu-id="5b407-117">此工作只會在現有的互動式會話中執行。</span><span class="sxs-lookup"><span data-stu-id="5b407-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5b407-118">InteractiveTokenOrPassword</span><span class="sxs-lookup"><span data-stu-id="5b407-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="5b407-119">不再使用;目前與密碼相同。</span><span class="sxs-lookup"><span data-stu-id="5b407-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="5b407-120">**Windows 10、1511版、Windows 10、1507版、Windows 8.1、Windows server 2012 R2、Windows 8、Windows server 2012、Windows Vista 和 Windows server 2008：** 工作將在現有的互動式會話中執行，或使用者必須使用密碼登入。</span><span class="sxs-lookup"><span data-stu-id="5b407-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5b407-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b407-121">Requirements</span></span>



| <span data-ttu-id="5b407-122">需求</span><span class="sxs-lookup"><span data-stu-id="5b407-122">Requirement</span></span> | <span data-ttu-id="5b407-123">值</span><span class="sxs-lookup"><span data-stu-id="5b407-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b407-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b407-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5b407-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b407-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5b407-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b407-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5b407-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b407-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b407-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b407-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b407-129">工作排程器架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="5b407-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5b407-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="5b407-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





