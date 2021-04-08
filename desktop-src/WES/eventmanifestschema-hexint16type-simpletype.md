---
title: UInt16Type 簡單類型
description: 定義不帶正負號的短型別。
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- UInt16Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686340"
---
# <a name="uint16type-simple-type"></a><span data-ttu-id="ef410-104">UInt16Type 簡單類型</span><span class="sxs-lookup"><span data-stu-id="ef410-104">UInt16Type Simple Type</span></span>

<span data-ttu-id="ef410-105">定義不帶正負號的短型別。</span><span class="sxs-lookup"><span data-stu-id="ef410-105">Defines an unsigned short type.</span></span> <span data-ttu-id="ef410-106">值可以指定為0到65535範圍內的2位元組整數或十六進位值。</span><span class="sxs-lookup"><span data-stu-id="ef410-106">The value can be specified as a 2-byte integer or hexadecimal value in the range from 0 through 65,535.</span></span>

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="ef410-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef410-107">Requirements</span></span>



| <span data-ttu-id="ef410-108">需求</span><span class="sxs-lookup"><span data-stu-id="ef410-108">Requirement</span></span> | <span data-ttu-id="ef410-109">值</span><span class="sxs-lookup"><span data-stu-id="ef410-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef410-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef410-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ef410-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef410-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef410-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef410-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ef410-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef410-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





