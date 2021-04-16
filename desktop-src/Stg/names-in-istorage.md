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
# <a name="names-in-istorage"></a>IStorage 中的名稱

屬性集是使用格式識別碼來識別， (FMTID) 在 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面中。 在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面中，屬性集的命名方式是以 null 終止的 Unicode 字串，最大長度為32個字元。 若要啟用互通性，必須建立 FMTID 和對應的 null 終止 Unicode 字串之間的對應。

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>將屬性集從 FMTID 轉換成字串名稱

從 FMTID 轉換為對應的 Unicode 字串名稱時，請先確認 FMTID 是已知的值，如下表所列。 如果是的話，請使用對應的已知字串名稱。

| FMTID                                                                                | 名稱字串                       | 語義                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | COM2 摘要資訊                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Office 檔摘要資訊和使用者定義屬性。 |



 

> [!Note]  
> **DocumentSummaryInformation** 和 **使用者** 設定的屬性集是唯一的，因為它包含兩個區段。 任何其他屬性集都不允許有多個區段。 如需詳細資訊，請參閱 [結構化儲存體序列化屬性集格式](structured-storage-serialized-property-set-format.md)，以及 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)。 第一個區段已定義為 COM 的一部分;第二個是由 Microsoft Office 定義。

 

如果 FMTID 不是已知的值，請使用下列程式來演算法字串名稱的表單。

**若要演算法表單字串名稱**

1.  如有必要，請將 FMTID 轉換為位元組由小到小的位元組順序。
2.  採用 FMTID 的128位，將每個位元組串連在一起，將其視為一個長位字串。 128位值的第一個位是 FMTID 記憶體中第一個位元組的最少有效位;128位值的最後一個位是 FMTID 記憶體中最後一個位元組的最高有效位。 藉由在結尾加上兩個零位，將這些128位延伸至130位。
3.  將130位分為五個位的群組;這類群組將會有26個。 將每個群組視為具有反轉位優先順序的整數。 例如，128位的第一個是第一個五個位群組中最不重要的位;128位的第五個是第一個群組的最高有效位。
4.  將這些整數對應為32字元陣列中的索引： ABCDEFGHIJKLMNOPQRSTUVWXYZ012345。 這會產生一系列的26個 Unicode 字元，其中只使用大寫字元和數位。 不適用區分大小寫及不區分大小寫的考慮，會導致每個字元在任何地區設定中都是唯一的。
5.  將字串 " \\ 005" 串連至這些26個字元的前方，以建立最終字串，總計長度為27個字元。

下列範例程式碼示範如何從 FMTID 對應至屬性字串。


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>將屬性集從字串名稱轉換成 FMTID

屬性字串名稱至 Guid 的轉換器應接受小寫字母，以與其大寫對應專案同義。

下列範例程式碼示範如何從屬性字串對應至 FMTID。


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



當嘗試開啟現有的屬性集時，在 [IPropertySetStorage：： open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)中， (根) FMTID 會轉換成字串（如上所述）。 如果該名稱的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 專案存在，就會使用它。 否則，開啟會失敗。

建立新的屬性集時，上述對應會決定所使用的字串名稱。

 

 





