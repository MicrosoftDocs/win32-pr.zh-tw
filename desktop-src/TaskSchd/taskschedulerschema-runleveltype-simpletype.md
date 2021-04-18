---
title: runLevelType 簡單類型
description: 定義 RunLevel (principalType) 元素的可能值。
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- runLevelType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965318"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="87819-104">runLevelType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="87819-104">runLevelType Simple Type</span></span>

<span data-ttu-id="87819-105">定義 [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) 元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="87819-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="87819-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="87819-106">Enumeration values</span></span>

<span data-ttu-id="87819-107">**RunLevelType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="87819-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="87819-108">值</span><span class="sxs-lookup"><span data-stu-id="87819-108">Value</span></span>            | <span data-ttu-id="87819-109">描述</span><span class="sxs-lookup"><span data-stu-id="87819-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="87819-110">LeastPrivilege</span><span class="sxs-lookup"><span data-stu-id="87819-110">LeastPrivilege</span></span>   | <span data-ttu-id="87819-111">工作會以最少的許可權執行， (LUA) 。</span><span class="sxs-lookup"><span data-stu-id="87819-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="87819-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="87819-112">HighestAvailable</span></span> | <span data-ttu-id="87819-113">工作是以最高許可權執行。</span><span class="sxs-lookup"><span data-stu-id="87819-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="87819-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="87819-114">Requirements</span></span>



| <span data-ttu-id="87819-115">需求</span><span class="sxs-lookup"><span data-stu-id="87819-115">Requirement</span></span> | <span data-ttu-id="87819-116">值</span><span class="sxs-lookup"><span data-stu-id="87819-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87819-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87819-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87819-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87819-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87819-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87819-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87819-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87819-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





