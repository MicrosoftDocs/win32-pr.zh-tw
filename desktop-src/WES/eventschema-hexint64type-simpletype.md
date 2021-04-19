---
title: 'HexInt64Type 簡單類型 (事件架構) '
description: '定義8位元組的十六進位型別。 |HexInt64Type 簡單類型 (事件架構) '
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- HexInt64Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107001783"
---
# <a name="hexint64type-simple-type-event-schema"></a><span data-ttu-id="d52c4-105">HexInt64Type 簡單類型 (事件架構) </span><span class="sxs-lookup"><span data-stu-id="d52c4-105">HexInt64Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="d52c4-106">定義8位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="d52c4-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="d52c4-107">模式</span><span class="sxs-lookup"><span data-stu-id="d52c4-107">Patterns</span></span>

<span data-ttu-id="d52c4-108">**HexInt64Type** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="d52c4-108">The **HexInt64Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="d52c4-109">值可以包含一到十六個十六進位字元 (例如0xa 或 0xac7bd361004fe190) 。</span><span class="sxs-lookup"><span data-stu-id="d52c4-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="d52c4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d52c4-110">Requirements</span></span>



| <span data-ttu-id="d52c4-111">需求</span><span class="sxs-lookup"><span data-stu-id="d52c4-111">Requirement</span></span> | <span data-ttu-id="d52c4-112">值</span><span class="sxs-lookup"><span data-stu-id="d52c4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d52c4-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d52c4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d52c4-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d52c4-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d52c4-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d52c4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d52c4-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d52c4-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





