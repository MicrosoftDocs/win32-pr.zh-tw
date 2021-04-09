---
title: 'UInt64Type 簡單類型 (EventManifest 架構) '
description: 定義不帶正負號的 long 類型。
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- UInt64Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025050"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="fd136-104">UInt64Type 簡單類型</span><span class="sxs-lookup"><span data-stu-id="fd136-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="fd136-105">定義不帶正負號的 long 類型。</span><span class="sxs-lookup"><span data-stu-id="fd136-105">Defines an unsigned long type.</span></span> <span data-ttu-id="fd136-106">值可以指定為0到18446744073709551615之間的8位元組整數或十六進位值。</span><span class="sxs-lookup"><span data-stu-id="fd136-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="fd136-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd136-107">Requirements</span></span>



| <span data-ttu-id="fd136-108">需求</span><span class="sxs-lookup"><span data-stu-id="fd136-108">Requirement</span></span> | <span data-ttu-id="fd136-109">值</span><span class="sxs-lookup"><span data-stu-id="fd136-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd136-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd136-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fd136-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd136-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd136-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd136-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fd136-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd136-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





