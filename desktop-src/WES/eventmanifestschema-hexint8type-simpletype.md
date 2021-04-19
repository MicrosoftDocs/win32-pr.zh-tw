---
title: UInt8Type 簡單類型
description: 定義不帶正負號的位元組類型。
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- UInt8Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966309"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="a7d04-104">UInt8Type 簡單類型</span><span class="sxs-lookup"><span data-stu-id="a7d04-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="a7d04-105">定義不帶正負號的位元組類型。</span><span class="sxs-lookup"><span data-stu-id="a7d04-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="a7d04-106">值可以指定為0到255範圍內的1位元組整數或十六進位值。</span><span class="sxs-lookup"><span data-stu-id="a7d04-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="a7d04-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7d04-107">Requirements</span></span>



| <span data-ttu-id="a7d04-108">需求</span><span class="sxs-lookup"><span data-stu-id="a7d04-108">Requirement</span></span> | <span data-ttu-id="a7d04-109">值</span><span class="sxs-lookup"><span data-stu-id="a7d04-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7d04-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7d04-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d04-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7d04-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a7d04-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7d04-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d04-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7d04-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





