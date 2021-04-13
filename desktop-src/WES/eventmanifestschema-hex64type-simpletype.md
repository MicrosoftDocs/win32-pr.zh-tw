---
title: HexInt64Type 簡單類型
description: 定義8位元組的十六進位型別。 |HexInt64Type 簡單類型
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
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
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386365"
---
# <a name="hexint64type-simple-type"></a><span data-ttu-id="76add-105">HexInt64Type 簡單類型</span><span class="sxs-lookup"><span data-stu-id="76add-105">HexInt64Type Simple Type</span></span>

<span data-ttu-id="76add-106">定義8位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="76add-106">Defines an 8-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="76add-107">模式</span><span class="sxs-lookup"><span data-stu-id="76add-107">Patterns</span></span>

<span data-ttu-id="76add-108">**HexInt64Type** 簡單類型是以下列模式限制的 [字串](/dotnet/api/system.string)：</span><span class="sxs-lookup"><span data-stu-id="76add-108">The **HexInt64Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="76add-109">值可以包含一到十六個十六進位字元 (例如0xa 或 0xac7bd361004fe190) 。</span><span class="sxs-lookup"><span data-stu-id="76add-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="76add-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="76add-110">Requirements</span></span>



| <span data-ttu-id="76add-111">需求</span><span class="sxs-lookup"><span data-stu-id="76add-111">Requirement</span></span> | <span data-ttu-id="76add-112">值</span><span class="sxs-lookup"><span data-stu-id="76add-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76add-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76add-113">Minimum supported client</span></span><br/> | <span data-ttu-id="76add-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76add-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76add-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76add-115">Minimum supported server</span></span><br/> | <span data-ttu-id="76add-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76add-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

