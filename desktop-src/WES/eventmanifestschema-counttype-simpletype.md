---
title: CountType 簡單類型
description: 定義用來指定陣列中元素數目的計數類型。
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- CountType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686596"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="e8fb8-104">CountType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="e8fb8-104">CountType Simple Type</span></span>

<span data-ttu-id="e8fb8-105">定義用來指定陣列中元素數目的計數類型。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="e8fb8-106">您可以將此值指定為 xs： unsignedShort 值，或指定為參考包含 unsiged short 值的資料項目節點名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="e8fb8-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8fb8-107">Requirements</span></span>



| <span data-ttu-id="e8fb8-108">需求</span><span class="sxs-lookup"><span data-stu-id="e8fb8-108">Requirement</span></span> | <span data-ttu-id="e8fb8-109">值</span><span class="sxs-lookup"><span data-stu-id="e8fb8-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8fb8-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8fb8-110">Minimum supported client</span></span><br/> | <span data-ttu-id="e8fb8-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8fb8-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8fb8-112">Minimum supported server</span></span><br/> | <span data-ttu-id="e8fb8-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





