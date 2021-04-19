---
description: 定義不帶正負號的整數類型。
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: 'UInt32Type 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974677"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="4ccdb-103">UInt32Type 簡單類型 (效能計數器) </span><span class="sxs-lookup"><span data-stu-id="4ccdb-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="4ccdb-104">定義不帶正負號的整數類型。</span><span class="sxs-lookup"><span data-stu-id="4ccdb-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="4ccdb-105">備註</span><span class="sxs-lookup"><span data-stu-id="4ccdb-105">Remarks</span></span>

<span data-ttu-id="4ccdb-106">您可以從0到4294967295的範圍中，將值指定為4個位元組的整數或十六進位值。</span><span class="sxs-lookup"><span data-stu-id="4ccdb-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ccdb-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ccdb-107">Requirements</span></span>



| <span data-ttu-id="4ccdb-108">需求</span><span class="sxs-lookup"><span data-stu-id="4ccdb-108">Requirement</span></span> | <span data-ttu-id="4ccdb-109">值</span><span class="sxs-lookup"><span data-stu-id="4ccdb-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ccdb-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ccdb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccdb-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ccdb-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ccdb-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ccdb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccdb-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ccdb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




