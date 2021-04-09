---
description: CInstance 類別會公開下列方法。
ms.assetid: B9846350-405D-440E-AC35-16446D3F03F5
ms.tgt_platform: multiple
title: CInstance 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e088f4604263d3fd1673982e22e2f6c88f991b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850784"
---
# <a name="cinstance-methods"></a><span data-ttu-id="f4f42-103">CInstance 方法</span><span class="sxs-lookup"><span data-stu-id="f4f42-103">CInstance Methods</span></span>

<span data-ttu-id="f4f42-104">\[[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="f4f42-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f4f42-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="f4f42-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f4f42-106">[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)類別會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="f4f42-106">The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f4f42-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="f4f42-107">In this section</span></span>

-   [<span data-ttu-id="f4f42-108">**Commit 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-108">**Commit method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-commit)
-   [<span data-ttu-id="f4f42-109">**Getbool 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-109">**Getbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbool)
-   [<span data-ttu-id="f4f42-110">**GetByte 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-110">**GetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbyte)
-   [<span data-ttu-id="f4f42-111">**GetCHString 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-111">**GetCHString method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getchstring)
-   [<span data-ttu-id="f4f42-112">**GetClassObjectInterface 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-112">**GetClassObjectInterface method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getclassobjectinterface)
-   [<span data-ttu-id="f4f42-113">**GetDateTime 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-113">**GetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdatetime)
-   [<span data-ttu-id="f4f42-114">**GetDOUBLE 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-114">**GetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdouble)
-   [<span data-ttu-id="f4f42-115">**GetDWORD 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-115">**GetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdword)
-   [<span data-ttu-id="f4f42-116">**GetEmbeddedObject 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-116">**GetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getembeddedobject)
-   [<span data-ttu-id="f4f42-117">**GetMethodCoNtext 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-117">**GetMethodContext method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getmethodcontext)
-   [<span data-ttu-id="f4f42-118">**GetStatus 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-118">**GetStatus method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstatus)
-   [<span data-ttu-id="f4f42-119">**GetStringArray 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-119">**GetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstringarray)
-   [<span data-ttu-id="f4f42-120">**GetTimeSpan 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-120">**GetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-gettimespan)
-   [<span data-ttu-id="f4f42-121">**GetVariant 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-121">**GetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getvariant)
-   [<span data-ttu-id="f4f42-122">**GetWBEMINT16 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-122">**GetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwbemint16)
-   [<span data-ttu-id="f4f42-123">**GetWBEMINT64 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-123">**GetWBEMINT64 methods**</span></span>](cinstance-getwbemint64.md)
-   [<span data-ttu-id="f4f42-124">**GetWCHAR 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-124">**GetWCHAR method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwchar)
-   [<span data-ttu-id="f4f42-125">**GetWORD 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-125">**GetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getword)
-   [<span data-ttu-id="f4f42-126">**IsNull 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-126">**IsNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-isnull)
-   [<span data-ttu-id="f4f42-127">**Setbool 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-127">**Setbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbool)
-   [<span data-ttu-id="f4f42-128">**SetByte 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-128">**SetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbyte)
-   [<span data-ttu-id="f4f42-129">**SetCharSplat 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-129">**SetCharSplat methods**</span></span>](cinstance-setcharsplat.md)
-   [<span data-ttu-id="f4f42-130">**SetCHString 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-130">**SetCHString methods**</span></span>](cinstance-setchstring.md)
-   [<span data-ttu-id="f4f42-131">**SetDateTime 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-131">**SetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdatetime)
-   [<span data-ttu-id="f4f42-132">**SetDOUBLE 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-132">**SetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdouble)
-   [<span data-ttu-id="f4f42-133">**SetDWORD 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-133">**SetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdword)
-   [<span data-ttu-id="f4f42-134">**SetEmbeddedObject 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-134">**SetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setembeddedobject)
-   [<span data-ttu-id="f4f42-135">**SetNull 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-135">**SetNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setnull)
-   [<span data-ttu-id="f4f42-136">**SetStringArray 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-136">**SetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setstringarray)
-   [<span data-ttu-id="f4f42-137">**SetTimeSpan 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-137">**SetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-settimespan)
-   [<span data-ttu-id="f4f42-138">**SetVariant 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-138">**SetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setvariant)
-   [<span data-ttu-id="f4f42-139">**SetWBEMINT16 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-139">**SetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwbemint16)
-   [<span data-ttu-id="f4f42-140">**SetWCHARSplat 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-140">**SetWCHARSplat method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwcharsplat)
-   <span data-ttu-id="f4f42-141">[**SetWBEMINT64 方法**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4f42-141">[**SetWBEMINT64 methods**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span></span>
-   [<span data-ttu-id="f4f42-142">**SetWORD 方法**</span><span class="sxs-lookup"><span data-stu-id="f4f42-142">**SetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setword)

 

 
