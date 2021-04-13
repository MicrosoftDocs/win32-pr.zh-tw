---
title: processTokenSidType 簡單類型
description: 定義 ProcessTokenSidType (principalType) 元素的可能值。
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- processTokenSidType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384354"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="30134-104">processTokenSidType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="30134-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="30134-105">定義 [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) 元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="30134-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="30134-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="30134-106">Enumeration values</span></span>

<span data-ttu-id="30134-107">**ProcessTokenSidType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="30134-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="30134-108">值</span><span class="sxs-lookup"><span data-stu-id="30134-108">Value</span></span>        | <span data-ttu-id="30134-109">描述</span><span class="sxs-lookup"><span data-stu-id="30134-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30134-110">無</span><span class="sxs-lookup"><span data-stu-id="30134-110">None</span></span>         | <span data-ttu-id="30134-111">工作會在不包含處理常式權杖 SID 的進程中執行， (進程權杖群組清單) 不會進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="30134-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="30134-112">不受限制</span><span class="sxs-lookup"><span data-stu-id="30134-112">Unrestricted</span></span> | <span data-ttu-id="30134-113">工作 SID 將衍生自完整的工作路徑，並新增至 [處理權杖群組] 清單。</span><span class="sxs-lookup"><span data-stu-id="30134-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="30134-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="30134-114">Requirements</span></span>



| <span data-ttu-id="30134-115">需求</span><span class="sxs-lookup"><span data-stu-id="30134-115">Requirement</span></span> | <span data-ttu-id="30134-116">值</span><span class="sxs-lookup"><span data-stu-id="30134-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="30134-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30134-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30134-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30134-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="30134-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30134-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30134-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30134-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





