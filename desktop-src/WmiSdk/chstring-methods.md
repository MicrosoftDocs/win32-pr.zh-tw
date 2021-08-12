---
description: CHString 類別會公開下列方法。
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: CHString 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d15726702177aa484a070cca3ec1aab56d708b57991d3ff6a7aae43b1ccf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556953"
---
# <a name="chstring-methods"></a>CHString 方法

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

[**CHString**](chstring.md)類別會公開下列方法。

## <a name="in-this-section"></a>本節內容

-   [**AllocSysString 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**CHString 函式**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**Collate 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**CompareNoCase 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Empty 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Find 方法**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**FindOneOf 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**格式方法**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**FormatMessageW 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**FormatV 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**FreeExtra 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**GetAllocLength 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**GetAt 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**GetBufferSetLength 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**的一種方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**GetLength 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Left 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**LoadStringW 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**LockBuffer 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**MakeLower 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**MakeReverse 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**MakeUpper 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Mid 方法**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**operator \[ \] 方法**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString：： operator +**](chstring--operator-plus.md)
-   [**CHString：： operator + =**](chstring--operator-plus-equal.md)
-   [**CHString：： operator =**](chstring--operator-equal.md)
-   [**operator = = (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**operator = = (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**operator> (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**operator> (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**operator>= (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**operator>= (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**operator< (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**operator< (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**operator<= (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**operator<= (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**operator！ = (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**operator！ = (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**operator LPCWSTR 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**ReleaseBuffer 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**ReverseFind 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Right 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**SetAt 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**SpanExcluding 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**SpanIncluding 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**TrimLeft 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**TrimRight 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**UnlockBuffer 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
