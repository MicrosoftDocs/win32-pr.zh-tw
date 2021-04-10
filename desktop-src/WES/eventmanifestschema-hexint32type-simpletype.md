---
title: 'UInt32Type 簡單類型 (Windows 事件記錄檔) '
description: 定義不帶正負號的整數類型。
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- UInt32Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934326"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="fd03a-104">UInt32Type 簡單類型 (Windows 事件記錄檔) </span><span class="sxs-lookup"><span data-stu-id="fd03a-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="fd03a-105">定義不帶正負號的整數類型。</span><span class="sxs-lookup"><span data-stu-id="fd03a-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="fd03a-106">值可以指定為0到4294967295範圍內的4位元組整數或十六進位值。</span><span class="sxs-lookup"><span data-stu-id="fd03a-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="fd03a-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd03a-107">Requirements</span></span>



| <span data-ttu-id="fd03a-108">需求</span><span class="sxs-lookup"><span data-stu-id="fd03a-108">Requirement</span></span> | <span data-ttu-id="fd03a-109">值</span><span class="sxs-lookup"><span data-stu-id="fd03a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd03a-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd03a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fd03a-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd03a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd03a-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd03a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fd03a-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd03a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





