---
description: 定義4位元組的十六進位型別。
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: 'HexInt32Type 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983638"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="dd6d8-103">HexInt32Type 簡單類型 (效能計數器) </span><span class="sxs-lookup"><span data-stu-id="dd6d8-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="dd6d8-104">定義4位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="dd6d8-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="dd6d8-105">模式</span><span class="sxs-lookup"><span data-stu-id="dd6d8-105">Patterns</span></span>

<span data-ttu-id="dd6d8-106">**HexInt32Type** 簡單類型是以下列模式限制的 **xs： string** ：</span><span class="sxs-lookup"><span data-stu-id="dd6d8-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="dd6d8-107">值可以包含一到八個十六進位字元 (例如0xa 或 0xac7bd361) 。</span><span class="sxs-lookup"><span data-stu-id="dd6d8-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6d8-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd6d8-108">Requirements</span></span>



| <span data-ttu-id="dd6d8-109">需求</span><span class="sxs-lookup"><span data-stu-id="dd6d8-109">Requirement</span></span> | <span data-ttu-id="dd6d8-110">值</span><span class="sxs-lookup"><span data-stu-id="dd6d8-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd6d8-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd6d8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6d8-112">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd6d8-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd6d8-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd6d8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6d8-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd6d8-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




