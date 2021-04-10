---
title: 屬性集顯示名稱字典
description: 屬性顯示名稱的字典可讓屬性（property）使用者將意義附加至屬性，而不是由類型指標所提供的屬性。
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682800"
---
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="e8721-103">屬性集顯示名稱字典</span><span class="sxs-lookup"><span data-stu-id="e8721-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="e8721-104">屬性顯示名稱的字典可讓屬性（property）使用者將意義附加至屬性，而不是由類型指標所提供的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8721-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="e8721-105">字典結構</span><span class="sxs-lookup"><span data-stu-id="e8721-105">Dictionary Structure</span></span>

<span data-ttu-id="e8721-106">字典包含清單中的專案計數，後面接著字典專案的清單。</span><span class="sxs-lookup"><span data-stu-id="e8721-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="e8721-107">字典輸入結構</span><span class="sxs-lookup"><span data-stu-id="e8721-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="e8721-108">清單中的每個字典專案都是屬性識別碼/字串配對。</span><span class="sxs-lookup"><span data-stu-id="e8721-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="e8721-109">以下是字典專案的虛擬結構定義。</span><span class="sxs-lookup"><span data-stu-id="e8721-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="e8721-110">它是虛擬結構，因為 sz 成員的 \[ \] 大小是可變的。</span><span class="sxs-lookup"><span data-stu-id="e8721-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="e8721-111">範例字典</span><span class="sxs-lookup"><span data-stu-id="e8721-111">Sample Dictionary</span></span>

<span data-ttu-id="e8721-112">下列股票市場資料傳輸範例可能會在整個集合中包含可顯示的名稱「股票報價」，以及 PID 符號的「代號符號」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e8721-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="e8721-113">如果屬性集只包含符號和字典，屬性集區段會有如下所示的位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="e8721-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

<span data-ttu-id="e8721-114">請注意下列有關屬性集字典的問題：</span><span class="sxs-lookup"><span data-stu-id="e8721-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="e8721-115">屬性識別碼0沒有類型指標。</span><span class="sxs-lookup"><span data-stu-id="e8721-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="e8721-116">**DWORD** 資料類型，指出位於類型指標位置的專案計數。</span><span class="sxs-lookup"><span data-stu-id="e8721-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="e8721-117">*Cch* 字串中的字元計數包含終止字串的零個字元。</span><span class="sxs-lookup"><span data-stu-id="e8721-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="e8721-118">當屬性集的字碼頁不是 Unicode 時，此欄位實際上是 **位元組** 計數。</span><span class="sxs-lookup"><span data-stu-id="e8721-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="e8721-119">若是格式為0的屬性集，這個計數可能不會超過256。</span><span class="sxs-lookup"><span data-stu-id="e8721-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="e8721-120">針對格式為1的屬性集，這個計數可能會和 total property set 大小所允許的大小一樣大。</span><span class="sxs-lookup"><span data-stu-id="e8721-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="e8721-121">字典是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e8721-121">The dictionary is optional.</span></span> <span data-ttu-id="e8721-122">並非集合中的所有屬性名稱都必須出現在字典中。</span><span class="sxs-lookup"><span data-stu-id="e8721-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="e8721-123">相反地，並非字典中的所有名稱都需要對應至集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8721-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="e8721-124">字典應該略過屬性的專案，而這些屬性是由操作屬性集的應用程式所被視為普遍辨識的。</span><span class="sxs-lookup"><span data-stu-id="e8721-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="e8721-125">一般而言，會省略廣泛接受標準的基底屬性集名稱，但特殊用途的屬性集可能包含瀏覽器所使用的字典。</span><span class="sxs-lookup"><span data-stu-id="e8721-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="e8721-126">字典中的屬性名稱會儲存在由 [屬性識別碼 1](/windows/desktop/Stg/reserved-property-identifiers)指出的字碼頁中。</span><span class="sxs-lookup"><span data-stu-id="e8721-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="e8721-127">針對 ANSI 字碼頁，每個字典專案都是以位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="e8721-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="e8721-128">因此，屬性識別碼為0的屬性名稱之間沒有間距。</span><span class="sxs-lookup"><span data-stu-id="e8721-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="e8721-129">這是在32位界限上，不需要對齊 **DWORD** 資料類型 (屬性識別碼和屬性名稱長度 **DWORD** s) 值的唯一情況。</span><span class="sxs-lookup"><span data-stu-id="e8721-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="e8721-130">若為 Unicode 頁面，每個字典專案都會對齊32位。</span><span class="sxs-lookup"><span data-stu-id="e8721-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="e8721-131">以二進位 Unicode 字元（以0x0001 到0x001F）開頭的屬性名稱會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="e8721-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="e8721-132">與屬性識別碼0相關聯的屬性名稱代表整個屬性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8721-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 