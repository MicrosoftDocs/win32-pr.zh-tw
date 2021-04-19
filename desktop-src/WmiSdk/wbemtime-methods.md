---
description: WBEMTime 類別會公開下列方法。
ms.assetid: 56B21156-8FD2-4FF8-805E-DDA63C897F80
ms.tgt_platform: multiple
title: WBEMTime 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e77c338f3d1d0657e20bfe6b819c9976d00d45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979413"
---
# <a name="wbemtime-methods"></a><span data-ttu-id="78142-103">WBEMTime 方法</span><span class="sxs-lookup"><span data-stu-id="78142-103">WBEMTime Methods</span></span>

<span data-ttu-id="78142-104">\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="78142-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="78142-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="78142-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="78142-106">[**WBEMTime**](wbemtime.md)類別會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="78142-106">The [**WBEMTime**](wbemtime.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78142-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="78142-107">In this section</span></span>

-   [<span data-ttu-id="78142-108">**Clear 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-108">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)
-   [<span data-ttu-id="78142-109">**GetBSTR 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-109">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)
-   [<span data-ttu-id="78142-110">**GetDMTF 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-110">**GetDMTF method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)
-   [<span data-ttu-id="78142-111">**GetDMTFNonNtfs 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-111">**GetDMTFNonNtfs method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)
-   [<span data-ttu-id="78142-112">**GetFILETIME 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-112">**GetFILETIME method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)
-   <span data-ttu-id="78142-113">[**GetLocalOffsetForDate 方法**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78142-113">[**GetLocalOffsetForDate methods**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85))</span></span>
-   [<span data-ttu-id="78142-114">**GetStructtm 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-114">**GetStructtm method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)
-   [<span data-ttu-id="78142-115">**GetSYSTEMTIME 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-115">**GetSYSTEMTIME method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)
-   [<span data-ttu-id="78142-116">**GetTime 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-116">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)
-   [<span data-ttu-id="78142-117">**Gettime \_ t 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-117">**Gettime\_t method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)
-   [<span data-ttu-id="78142-118">**>isok 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-118">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)
-   <span data-ttu-id="78142-119">[**operator-運算子**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78142-119">[**operator- operators**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))</span></span>
-   [<span data-ttu-id="78142-120">**WBEMTime：： operator！ = 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-120">**WBEMTime::operator != method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)
-   [<span data-ttu-id="78142-121">**WBEMTime：： operator < 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-121">**WBEMTime::operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)
-   [<span data-ttu-id="78142-122">**WBEMTime：： operator <= 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-122">**WBEMTime::operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)
-   [<span data-ttu-id="78142-123">**WBEMTime：： operator = = 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-123">**WBEMTime::operator == method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)
-   [<span data-ttu-id="78142-124">**WBEMTime：： operator > 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-124">**WBEMTime::operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="78142-125">**WBEMTime：： operator >= 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-125">**WBEMTime::operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="78142-126">**operator + 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-126">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="78142-127">**operator + = 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-127">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   <span data-ttu-id="78142-128">[**operator = 運算子**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78142-128">[**operator= operators**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))</span></span>
-   [<span data-ttu-id="78142-129">**operator-= 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-129">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="78142-130">**SetDMTF 方法**</span><span class="sxs-lookup"><span data-stu-id="78142-130">**SetDMTF method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)
-   <span data-ttu-id="78142-131">[**WBEMTime 函式**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="78142-131">[**WBEMTime constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>

 

 
