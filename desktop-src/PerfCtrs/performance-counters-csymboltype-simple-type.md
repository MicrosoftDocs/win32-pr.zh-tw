---
description: CSymbolType 簡單類型 (效能計數器) -定義有效的 C/c + + 符號名稱。
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: 'CSymbolType 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084226"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="8588f-103">CSymbolType 簡單類型 (效能計數器) </span><span class="sxs-lookup"><span data-stu-id="8588f-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="8588f-104">定義有效的 C/c + + 符號名稱。</span><span class="sxs-lookup"><span data-stu-id="8588f-104">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="8588f-105">模式</span><span class="sxs-lookup"><span data-stu-id="8588f-105">Patterns</span></span>

<span data-ttu-id="8588f-106">**CSymbolType** 簡單類型是以下列模式限制的 **xs： string** ：</span><span class="sxs-lookup"><span data-stu-id="8588f-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="8588f-107">符號名稱可以是空的，或包含英數位元和底線。</span><span class="sxs-lookup"><span data-stu-id="8588f-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="8588f-108">如果您指定名稱，則名稱必須以底線 (開頭 \_) 或字母字元。</span><span class="sxs-lookup"><span data-stu-id="8588f-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="8588f-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8588f-109">Requirements</span></span>



| <span data-ttu-id="8588f-110">需求</span><span class="sxs-lookup"><span data-stu-id="8588f-110">Requirement</span></span> | <span data-ttu-id="8588f-111">值</span><span class="sxs-lookup"><span data-stu-id="8588f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8588f-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8588f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8588f-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8588f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8588f-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8588f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8588f-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8588f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




