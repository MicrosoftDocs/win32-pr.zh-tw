---
title: 'HexInt32Type 簡單類型 (事件架構) '
description: '定義4位元組的十六進位型別。 |HexInt32Type 簡單類型 (事件架構) '
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- HexInt32Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945868"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="09c79-105">HexInt32Type 簡單類型 (事件架構) </span><span class="sxs-lookup"><span data-stu-id="09c79-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="09c79-106">定義4位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="09c79-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="09c79-107">模式</span><span class="sxs-lookup"><span data-stu-id="09c79-107">Patterns</span></span>

<span data-ttu-id="09c79-108">**HexInt32Type** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="09c79-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="09c79-109">值可以包含一到八個十六進位字元 (例如0xa 或 0xac7bd361) 。</span><span class="sxs-lookup"><span data-stu-id="09c79-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="09c79-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="09c79-110">Requirements</span></span>



| <span data-ttu-id="09c79-111">需求</span><span class="sxs-lookup"><span data-stu-id="09c79-111">Requirement</span></span> | <span data-ttu-id="09c79-112">值</span><span class="sxs-lookup"><span data-stu-id="09c79-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09c79-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09c79-113">Minimum supported client</span></span><br/> | <span data-ttu-id="09c79-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09c79-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09c79-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09c79-115">Minimum supported server</span></span><br/> | <span data-ttu-id="09c79-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09c79-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





