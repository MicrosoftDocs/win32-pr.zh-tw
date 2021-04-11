---
description: 定義有效的 C/c + + 符號名稱。
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: 'CSymbolType 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944250"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="d8296-103">CSymbolType 簡單類型 (效能計數器) </span><span class="sxs-lookup"><span data-stu-id="d8296-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="d8296-104">定義有效的 C/c + + 符號名稱。</span><span class="sxs-lookup"><span data-stu-id="d8296-104">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="d8296-105">模式</span><span class="sxs-lookup"><span data-stu-id="d8296-105">Patterns</span></span>

<span data-ttu-id="d8296-106">**CSymbolType** 簡單類型是以下列模式限制的 **xs： string** ：</span><span class="sxs-lookup"><span data-stu-id="d8296-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="d8296-107">符號名稱可以是空的，或包含英數位元和底線。</span><span class="sxs-lookup"><span data-stu-id="d8296-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="d8296-108">如果您指定名稱，則名稱必須以底線 (開頭 \_) 或字母字元。</span><span class="sxs-lookup"><span data-stu-id="d8296-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8296-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8296-109">Requirements</span></span>



| <span data-ttu-id="d8296-110">需求</span><span class="sxs-lookup"><span data-stu-id="d8296-110">Requirement</span></span> | <span data-ttu-id="d8296-111">值</span><span class="sxs-lookup"><span data-stu-id="d8296-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8296-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8296-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d8296-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8296-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8296-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8296-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d8296-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8296-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




