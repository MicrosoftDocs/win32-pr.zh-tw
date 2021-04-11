---
description: CHString 類別會公開下列方法。
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: CHString 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026964"
---
# <a name="chstring-methods"></a><span data-ttu-id="0cf36-103">CHString 方法</span><span class="sxs-lookup"><span data-stu-id="0cf36-103">CHString Methods</span></span>

<span data-ttu-id="0cf36-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="0cf36-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0cf36-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="0cf36-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0cf36-106">[**CHString**](chstring.md)類別會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="0cf36-106">The [**CHString**](chstring.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0cf36-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="0cf36-107">In this section</span></span>

-   [<span data-ttu-id="0cf36-108">**AllocSysString 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-108">**AllocSysString method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   <span data-ttu-id="0cf36-109">[**CHString 函式**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="0cf36-109">[**CHString constructors**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span></span>
-   [<span data-ttu-id="0cf36-110">**Collate 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-110">**Collate method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [<span data-ttu-id="0cf36-111">**Compare 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-111">**Compare method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [<span data-ttu-id="0cf36-112">**CompareNoCase 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-112">**CompareNoCase method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [<span data-ttu-id="0cf36-113">**Empty 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-113">**Empty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   <span data-ttu-id="0cf36-114">[**Find 方法**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span><span class="sxs-lookup"><span data-stu-id="0cf36-114">[**Find methods**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span></span>
-   [<span data-ttu-id="0cf36-115">**FindOneOf 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-115">**FindOneOf method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   <span data-ttu-id="0cf36-116">[**格式方法**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span><span class="sxs-lookup"><span data-stu-id="0cf36-116">[**Format methods**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span></span>
-   <span data-ttu-id="0cf36-117">[**FormatMessageW 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span><span class="sxs-lookup"><span data-stu-id="0cf36-117">[**FormatMessageW methods**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span></span>
-   [<span data-ttu-id="0cf36-118">**FormatV 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-118">**FormatV method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [<span data-ttu-id="0cf36-119">**FreeExtra 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-119">**FreeExtra method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [<span data-ttu-id="0cf36-120">**GetAllocLength 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-120">**GetAllocLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   <span data-ttu-id="0cf36-121">[**GetAt 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span><span class="sxs-lookup"><span data-stu-id="0cf36-121">[**GetAt method**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span></span>
-   [<span data-ttu-id="0cf36-122">**GetBuffer 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-122">**GetBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [<span data-ttu-id="0cf36-123">**GetBufferSetLength 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-123">**GetBufferSetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [<span data-ttu-id="0cf36-124">**的一種方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-124">**GetData method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [<span data-ttu-id="0cf36-125">**GetLength 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-125">**GetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [<span data-ttu-id="0cf36-126">**IsEmpty 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-126">**IsEmpty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [<span data-ttu-id="0cf36-127">**Left 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-127">**Left method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   <span data-ttu-id="0cf36-128">[**LoadStringW 方法**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span><span class="sxs-lookup"><span data-stu-id="0cf36-128">[**LoadStringW method**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span></span>
-   [<span data-ttu-id="0cf36-129">**LockBuffer 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-129">**LockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [<span data-ttu-id="0cf36-130">**MakeLower 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-130">**MakeLower method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [<span data-ttu-id="0cf36-131">**MakeReverse 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-131">**MakeReverse method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [<span data-ttu-id="0cf36-132">**MakeUpper 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-132">**MakeUpper method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   <span data-ttu-id="0cf36-133">[**Mid 方法**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="0cf36-133">[**Mid methods**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>
-   <span data-ttu-id="0cf36-134">[**operator \[ \] 方法**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-134">[**operator\[\] method**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span></span>
-   [<span data-ttu-id="0cf36-135">**CHString：： operator +**</span><span class="sxs-lookup"><span data-stu-id="0cf36-135">**CHString::operator+**</span></span>](chstring--operator-plus.md)
-   [<span data-ttu-id="0cf36-136">**CHString：： operator + =**</span><span class="sxs-lookup"><span data-stu-id="0cf36-136">**CHString::operator+=**</span></span>](chstring--operator-plus-equal.md)
-   [<span data-ttu-id="0cf36-137">**CHString：： operator =**</span><span class="sxs-lookup"><span data-stu-id="0cf36-137">**CHString::operator=**</span></span>](chstring--operator-equal.md)
-   <span data-ttu-id="0cf36-138">[**operator = = (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-138">[**operator==(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-139">[**operator = = (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-139">[**operator==(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-140">[**operator> (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-140">[**operator>(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-141">[**operator> (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-141">[**operator>(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-142">[**operator>= (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-142">[**operator>=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-143">[**operator>= (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-143">[**operator>=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-144">[**operator< (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-144">[**operator<(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-145">[**operator< (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-145">[**operator<(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-146">[**operator<= (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-146">[**operator<=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-147">[**operator<= (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-147">[**operator<=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-148">[**operator！ = (constCHString&，constCHString&) 方法**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-148">[**operator!=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span></span>
-   <span data-ttu-id="0cf36-149">[**operator！ = (constCHString&，constLPCWSTR&) 方法**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0cf36-149">[**operator!=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span></span>
-   [<span data-ttu-id="0cf36-150">**operator LPCWSTR 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-150">**operator LPCWSTR method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [<span data-ttu-id="0cf36-151">**ReleaseBuffer 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-151">**ReleaseBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [<span data-ttu-id="0cf36-152">**ReverseFind 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-152">**ReverseFind method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [<span data-ttu-id="0cf36-153">**Right 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-153">**Right method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [<span data-ttu-id="0cf36-154">**SetAt 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-154">**SetAt method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [<span data-ttu-id="0cf36-155">**SpanExcluding 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-155">**SpanExcluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [<span data-ttu-id="0cf36-156">**SpanIncluding 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-156">**SpanIncluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [<span data-ttu-id="0cf36-157">**TrimLeft 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-157">**TrimLeft method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [<span data-ttu-id="0cf36-158">**TrimRight 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-158">**TrimRight method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [<span data-ttu-id="0cf36-159">**UnlockBuffer 方法**</span><span class="sxs-lookup"><span data-stu-id="0cf36-159">**UnlockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
