---
description: 以登錄格式定義全域唯一識別碼型別。
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: 'GUIDType 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849281"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="c32d6-103">GUIDType 簡單類型 (效能計數器) </span><span class="sxs-lookup"><span data-stu-id="c32d6-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="c32d6-104">以登錄格式定義全域唯一識別碼型別。</span><span class="sxs-lookup"><span data-stu-id="c32d6-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="c32d6-105">模式</span><span class="sxs-lookup"><span data-stu-id="c32d6-105">Patterns</span></span>

<span data-ttu-id="c32d6-106">**GUIDType** 簡單類型是以下列模式限制的 **xs： string** ：</span><span class="sxs-lookup"><span data-stu-id="c32d6-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="c32d6-107">此值必須是登錄格式的全域唯一識別碼類型。</span><span class="sxs-lookup"><span data-stu-id="c32d6-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="c32d6-108">例如，{5b2fc63a-8af4-44cb-960c-aefdced908d6}。</span><span class="sxs-lookup"><span data-stu-id="c32d6-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="c32d6-109">使用 GUIDGen.exe 或 UUIDGen.exe 建立 GUID。</span><span class="sxs-lookup"><span data-stu-id="c32d6-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="c32d6-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c32d6-110">Requirements</span></span>



| <span data-ttu-id="c32d6-111">需求</span><span class="sxs-lookup"><span data-stu-id="c32d6-111">Requirement</span></span> | <span data-ttu-id="c32d6-112">值</span><span class="sxs-lookup"><span data-stu-id="c32d6-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c32d6-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c32d6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c32d6-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c32d6-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c32d6-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c32d6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c32d6-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c32d6-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




