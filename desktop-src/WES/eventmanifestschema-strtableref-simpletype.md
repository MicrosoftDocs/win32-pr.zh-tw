---
title: strTableRef 簡單類型
description: 定義字串，這個字串會參考資訊清單中的字串資料表中所定義的訊息字串，或是在 ( 的訊息中，) 檔案。
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- strTableRef 簡單類型 EventLog
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508723"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="770f8-104">strTableRef 簡單類型</span><span class="sxs-lookup"><span data-stu-id="770f8-104">strTableRef Simple Type</span></span>

<span data-ttu-id="770f8-105">定義字串，這個字串會參考資訊清單中的字串資料表中所定義的訊息字串，或是在 ( 的訊息中，) 檔案。</span><span class="sxs-lookup"><span data-stu-id="770f8-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="770f8-106">模式</span><span class="sxs-lookup"><span data-stu-id="770f8-106">Patterns</span></span>

<span data-ttu-id="770f8-107">**StrTableRef** 簡單類型是以下列模式限制的 **xs： string** ：</span><span class="sxs-lookup"><span data-stu-id="770f8-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="770f8-108">字串的格式必須是 $string。*stringid 指定* 或 $mc.*symbolid*。</span><span class="sxs-lookup"><span data-stu-id="770f8-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="770f8-109">如果字串的格式為，$string。*stringid 指定*，它必須參考資訊清單 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的字串。</span><span class="sxs-lookup"><span data-stu-id="770f8-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="770f8-110">如果字串的格式為 $mc *symbolid*，它必須參考訊息檔中定義的符號。</span><span class="sxs-lookup"><span data-stu-id="770f8-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="770f8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="770f8-111">Requirements</span></span>



| <span data-ttu-id="770f8-112">需求</span><span class="sxs-lookup"><span data-stu-id="770f8-112">Requirement</span></span> | <span data-ttu-id="770f8-113">值</span><span class="sxs-lookup"><span data-stu-id="770f8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="770f8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="770f8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="770f8-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="770f8-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="770f8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="770f8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="770f8-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="770f8-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





