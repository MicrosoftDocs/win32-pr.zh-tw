---
title: actionBaseType 複雜類型
description: 定義此型別之所有元素的 Id 屬性。
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- actionBaseType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8091456b2f09e6be5a332930d68960b2473acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105888"
---
# <a name="actionbasetype-complex-type"></a><span data-ttu-id="d7995-104">actionBaseType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="d7995-104">actionBaseType Complex Type</span></span>

<span data-ttu-id="d7995-105">定義此型別之所有元素的 Id 屬性。</span><span class="sxs-lookup"><span data-stu-id="d7995-105">Defines the Id attribute for all elements of this type.</span></span>

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="d7995-106">屬性</span><span class="sxs-lookup"><span data-stu-id="d7995-106">Attributes</span></span>



| <span data-ttu-id="d7995-107">名稱</span><span class="sxs-lookup"><span data-stu-id="d7995-107">Name</span></span> | <span data-ttu-id="d7995-108">類型</span><span class="sxs-lookup"><span data-stu-id="d7995-108">Type</span></span> | <span data-ttu-id="d7995-109">描述</span><span class="sxs-lookup"><span data-stu-id="d7995-109">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="d7995-110">id</span><span class="sxs-lookup"><span data-stu-id="d7995-110">id</span></span>   | <span data-ttu-id="d7995-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="d7995-111">ID</span></span>   | <span data-ttu-id="d7995-112">工作所執行之動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7995-112">Id of the action performed by the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d7995-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7995-113">Requirements</span></span>



| <span data-ttu-id="d7995-114">需求</span><span class="sxs-lookup"><span data-stu-id="d7995-114">Requirement</span></span> | <span data-ttu-id="d7995-115">值</span><span class="sxs-lookup"><span data-stu-id="d7995-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7995-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7995-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7995-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7995-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7995-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7995-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7995-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7995-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7995-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7995-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7995-121">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="d7995-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="d7995-122">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d7995-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





