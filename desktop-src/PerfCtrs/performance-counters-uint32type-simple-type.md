---
description: UInt32Type 簡單類型 (效能計數器) -定義不帶正負號的整數類型。
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: 'UInt32Type 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114576"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="c5e1b-103">UInt32Type 簡單類型 (效能計數器) </span><span class="sxs-lookup"><span data-stu-id="c5e1b-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="c5e1b-104">定義不帶正負號的整數類型。</span><span class="sxs-lookup"><span data-stu-id="c5e1b-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="c5e1b-105">備註</span><span class="sxs-lookup"><span data-stu-id="c5e1b-105">Remarks</span></span>

<span data-ttu-id="c5e1b-106">您可以從0到4294967295的範圍中，將值指定為4個位元組的整數或十六進位值。</span><span class="sxs-lookup"><span data-stu-id="c5e1b-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e1b-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5e1b-107">Requirements</span></span>



| <span data-ttu-id="c5e1b-108">需求</span><span class="sxs-lookup"><span data-stu-id="c5e1b-108">Requirement</span></span> | <span data-ttu-id="c5e1b-109">值</span><span class="sxs-lookup"><span data-stu-id="c5e1b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5e1b-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5e1b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e1b-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5e1b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5e1b-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5e1b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e1b-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5e1b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




