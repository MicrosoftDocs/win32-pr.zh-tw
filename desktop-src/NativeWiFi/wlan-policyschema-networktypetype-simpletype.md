---
description: 定義無線網路類型。
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: networkTypeType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978336"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="766fd-103">networkTypeType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="766fd-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="766fd-104">NetworkTypeType 簡單類型會定義無線網路類型。</span><span class="sxs-lookup"><span data-stu-id="766fd-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="766fd-105">網路類型有兩種：基礎結構網路 (ESS) 和臨機操作網路 (IBSS) 。</span><span class="sxs-lookup"><span data-stu-id="766fd-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="766fd-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="766fd-106">Enumeration values</span></span>

<span data-ttu-id="766fd-107">**NetworkTypeType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="766fd-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="766fd-108">值</span><span class="sxs-lookup"><span data-stu-id="766fd-108">Value</span></span> | <span data-ttu-id="766fd-109">描述</span><span class="sxs-lookup"><span data-stu-id="766fd-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="766fd-110">IBSS</span><span class="sxs-lookup"><span data-stu-id="766fd-110">IBSS</span></span>  |             |
| <span data-ttu-id="766fd-111">Ess</span><span class="sxs-lookup"><span data-stu-id="766fd-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="766fd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="766fd-112">Requirements</span></span>



| <span data-ttu-id="766fd-113">需求</span><span class="sxs-lookup"><span data-stu-id="766fd-113">Requirement</span></span> | <span data-ttu-id="766fd-114">值</span><span class="sxs-lookup"><span data-stu-id="766fd-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="766fd-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="766fd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="766fd-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="766fd-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="766fd-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="766fd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="766fd-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="766fd-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




