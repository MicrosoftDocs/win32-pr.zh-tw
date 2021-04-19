---
title: 'HexInt32Type 簡單類型 (EventManifest 架構) '
description: '定義4位元組的十六進位型別。 |HexInt32Type 簡單類型 (EventManifest 架構) '
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
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
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992263"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a><span data-ttu-id="6cc08-105">HexInt32Type 簡單類型 (EventManifest 架構) </span><span class="sxs-lookup"><span data-stu-id="6cc08-105">HexInt32Type Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="6cc08-106">定義4位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="6cc08-106">Defines a 4-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="6cc08-107">模式</span><span class="sxs-lookup"><span data-stu-id="6cc08-107">Patterns</span></span>

<span data-ttu-id="6cc08-108">**HexInt32Type** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="6cc08-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="6cc08-109">值可以包含一到八個十六進位字元 (例如0xa 或 0xac7bd361) 。</span><span class="sxs-lookup"><span data-stu-id="6cc08-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc08-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cc08-110">Requirements</span></span>



| <span data-ttu-id="6cc08-111">需求</span><span class="sxs-lookup"><span data-stu-id="6cc08-111">Requirement</span></span> | <span data-ttu-id="6cc08-112">值</span><span class="sxs-lookup"><span data-stu-id="6cc08-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6cc08-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cc08-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc08-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cc08-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6cc08-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cc08-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc08-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cc08-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





