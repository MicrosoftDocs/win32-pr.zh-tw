---
title: HexInt8Type 簡單類型
description: 定義1位元組的十六進位型別。
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- HexInt8Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466965"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="280cb-104">HexInt8Type 簡單類型</span><span class="sxs-lookup"><span data-stu-id="280cb-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="280cb-105">定義1位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="280cb-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="280cb-106">模式</span><span class="sxs-lookup"><span data-stu-id="280cb-106">Patterns</span></span>

<span data-ttu-id="280cb-107">**HexInt8Type** 簡單類型是以下列模式限制的 [字串](/dotnet/api/system.string)：</span><span class="sxs-lookup"><span data-stu-id="280cb-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="280cb-108">值可以包含一到兩個十六進位字元 (例如，0xa 或 0xac) 。</span><span class="sxs-lookup"><span data-stu-id="280cb-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="280cb-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="280cb-109">Requirements</span></span>



| <span data-ttu-id="280cb-110">需求</span><span class="sxs-lookup"><span data-stu-id="280cb-110">Requirement</span></span> | <span data-ttu-id="280cb-111">值</span><span class="sxs-lookup"><span data-stu-id="280cb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="280cb-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="280cb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="280cb-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="280cb-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="280cb-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="280cb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="280cb-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="280cb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

