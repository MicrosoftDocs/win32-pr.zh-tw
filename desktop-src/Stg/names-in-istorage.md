---
title: IStorage 中的名稱
description: 屬性集是使用格式識別碼來識別， (FMTID) 在 IPropertySetStorage 介面中。
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507464"
---
# <a name="names-in-istorage"></a><span data-ttu-id="db2f8-103">IStorage 中的名稱</span><span class="sxs-lookup"><span data-stu-id="db2f8-103">Names in IStorage</span></span>

<span data-ttu-id="db2f8-104">屬性集是使用格式識別碼來識別， (FMTID) 在 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面中。</span><span class="sxs-lookup"><span data-stu-id="db2f8-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="db2f8-105">在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面中，屬性集的命名方式是以 null 終止的 Unicode 字串，最大長度為32個字元。</span><span class="sxs-lookup"><span data-stu-id="db2f8-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="db2f8-106">若要啟用互通性，必須建立 FMTID 和對應的 null 終止 Unicode 字串之間的對應。</span><span class="sxs-lookup"><span data-stu-id="db2f8-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="db2f8-107">將屬性集從 FMTID 轉換成字串名稱</span><span class="sxs-lookup"><span data-stu-id="db2f8-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="db2f8-108">從 FMTID 轉換為對應的 Unicode 字串名稱時，請先確認 FMTID 是已知的值，如下表所列。</span><span class="sxs-lookup"><span data-stu-id="db2f8-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="db2f8-109">如果是的話，請使用對應的已知字串名稱。</span><span class="sxs-lookup"><span data-stu-id="db2f8-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="db2f8-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="db2f8-110">FMTID</span></span>                                                                                | <span data-ttu-id="db2f8-111">名稱字串</span><span class="sxs-lookup"><span data-stu-id="db2f8-111">String name</span></span>                       | <span data-ttu-id="db2f8-112">語義</span><span class="sxs-lookup"><span data-stu-id="db2f8-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="db2f8-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="db2f8-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="db2f8-114">" \\ 005SummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="db2f8-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="db2f8-115">COM2 摘要資訊</span><span class="sxs-lookup"><span data-stu-id="db2f8-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="db2f8-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="db2f8-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="db2f8-117">" \\ 005DocumentSummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="db2f8-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="db2f8-118">Office 檔摘要資訊和使用者定義屬性。</span><span class="sxs-lookup"><span data-stu-id="db2f8-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="db2f8-119">**DocumentSummaryInformation** 和 **使用者** 設定的屬性集是唯一的，因為它包含兩個區段。</span><span class="sxs-lookup"><span data-stu-id="db2f8-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="db2f8-120">任何其他屬性集都不允許有多個區段。</span><span class="sxs-lookup"><span data-stu-id="db2f8-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="db2f8-121">如需詳細資訊，請參閱 [結構化儲存體序列化屬性集格式](structured-storage-serialized-property-set-format.md)，以及 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="db2f8-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="db2f8-122">第一個區段已定義為 COM 的一部分;第二個是由 Microsoft Office 定義。</span><span class="sxs-lookup"><span data-stu-id="db2f8-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="db2f8-123">如果 FMTID 不是已知的值，請使用下列程式來演算法字串名稱的表單。</span><span class="sxs-lookup"><span data-stu-id="db2f8-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="db2f8-124">**若要演算法表單字串名稱**</span><span class="sxs-lookup"><span data-stu-id="db2f8-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="db2f8-125">如有必要，請將 FMTID 轉換為位元組由小到小的位元組順序。</span><span class="sxs-lookup"><span data-stu-id="db2f8-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="db2f8-126">採用 FMTID 的128位，將每個位元組串連在一起，將其視為一個長位字串。</span><span class="sxs-lookup"><span data-stu-id="db2f8-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="db2f8-127">128位值的第一個位是 FMTID 記憶體中第一個位元組的最少有效位;128位值的最後一個位是 FMTID 記憶體中最後一個位元組的最高有效位。</span><span class="sxs-lookup"><span data-stu-id="db2f8-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="db2f8-128">藉由在結尾加上兩個零位，將這些128位延伸至130位。</span><span class="sxs-lookup"><span data-stu-id="db2f8-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="db2f8-129">將130位分為五個位的群組;這類群組將會有26個。</span><span class="sxs-lookup"><span data-stu-id="db2f8-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="db2f8-130">將每個群組視為具有反轉位優先順序的整數。</span><span class="sxs-lookup"><span data-stu-id="db2f8-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="db2f8-131">例如，128位的第一個是第一個五個位群組中最不重要的位;128位的第五個是第一個群組的最高有效位。</span><span class="sxs-lookup"><span data-stu-id="db2f8-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="db2f8-132">將這些整數對應為32字元陣列中的索引： ABCDEFGHIJKLMNOPQRSTUVWXYZ012345。</span><span class="sxs-lookup"><span data-stu-id="db2f8-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="db2f8-133">這會產生一系列的26個 Unicode 字元，其中只使用大寫字元和數位。</span><span class="sxs-lookup"><span data-stu-id="db2f8-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="db2f8-134">不適用區分大小寫及不區分大小寫的考慮，會導致每個字元在任何地區設定中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="db2f8-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="db2f8-135">將字串 " \\ 005" 串連至這些26個字元的前方，以建立最終字串，總計長度為27個字元。</span><span class="sxs-lookup"><span data-stu-id="db2f8-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="db2f8-136">下列範例程式碼示範如何從 FMTID 對應至屬性字串。</span><span class="sxs-lookup"><span data-stu-id="db2f8-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="db2f8-137">將屬性集從字串名稱轉換成 FMTID</span><span class="sxs-lookup"><span data-stu-id="db2f8-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="db2f8-138">屬性字串名稱至 Guid 的轉換器應接受小寫字母，以與其大寫對應專案同義。</span><span class="sxs-lookup"><span data-stu-id="db2f8-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="db2f8-139">下列範例程式碼示範如何從屬性字串對應至 FMTID。</span><span class="sxs-lookup"><span data-stu-id="db2f8-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="db2f8-140">當嘗試開啟現有的屬性集時，在 [IPropertySetStorage：： open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)中， (根) FMTID 會轉換成字串（如上所述）。</span><span class="sxs-lookup"><span data-stu-id="db2f8-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="db2f8-141">如果該名稱的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 專案存在，就會使用它。</span><span class="sxs-lookup"><span data-stu-id="db2f8-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="db2f8-142">否則，開啟會失敗。</span><span class="sxs-lookup"><span data-stu-id="db2f8-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="db2f8-143">建立新的屬性集時，上述對應會決定所使用的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="db2f8-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





