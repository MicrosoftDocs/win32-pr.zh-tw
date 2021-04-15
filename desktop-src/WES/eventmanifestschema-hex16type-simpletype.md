---
title: HexInt16Type 簡單類型
description: 定義2個位元組的十六進位型別。
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- HexInt16Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466605"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="3cca2-104">HexInt16Type 簡單類型</span><span class="sxs-lookup"><span data-stu-id="3cca2-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="3cca2-105">定義2個位元組的十六進位型別。</span><span class="sxs-lookup"><span data-stu-id="3cca2-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="3cca2-106">模式</span><span class="sxs-lookup"><span data-stu-id="3cca2-106">Patterns</span></span>

<span data-ttu-id="3cca2-107">**HexInt16Type** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="3cca2-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="3cca2-108">值可以包含一到四個十六進位字元 (例如0xa 或 0xac7b) 。</span><span class="sxs-lookup"><span data-stu-id="3cca2-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cca2-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cca2-109">Requirements</span></span>



| <span data-ttu-id="3cca2-110">需求</span><span class="sxs-lookup"><span data-stu-id="3cca2-110">Requirement</span></span> | <span data-ttu-id="3cca2-111">值</span><span class="sxs-lookup"><span data-stu-id="3cca2-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3cca2-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cca2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3cca2-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cca2-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3cca2-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cca2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3cca2-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cca2-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





