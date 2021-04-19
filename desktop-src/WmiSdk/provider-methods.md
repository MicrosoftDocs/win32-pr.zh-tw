---
description: Provider 類別會公開下列方法。
ms.assetid: AD0BCAC7-6B5C-4BAF-9641-37D315D3E7B1
ms.tgt_platform: multiple
title: 提供者方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb4d8f5d012b5209519670562a7f735a34e6f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994543"
---
# <a name="provider-methods"></a><span data-ttu-id="61113-103">提供者方法</span><span class="sxs-lookup"><span data-stu-id="61113-103">Provider Methods</span></span>

<span data-ttu-id="61113-104">\[[**提供者**](/windows/desktop/api/Provider/nl-provider-provider)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會有任何進一步的開發、增強功能或更新可用於影響這些程式庫的非安全性相關問題。</span><span class="sxs-lookup"><span data-stu-id="61113-104">\[The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="61113-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="61113-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="61113-106">[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)類別會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="61113-106">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61113-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="61113-107">In this section</span></span>

-   [<span data-ttu-id="61113-108">**Commit 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-108">**Commit method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-commit)
-   [<span data-ttu-id="61113-109">**CreateNewInstance 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-109">**CreateNewInstance method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-createnewinstance)
-   <span data-ttu-id="61113-110">[**DeleteInstance 方法**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="61113-110">[**DeleteInstance method**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span></span>
-   [<span data-ttu-id="61113-111">**EnumerateInstances 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-111">**EnumerateInstances method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-enumerateinstances)
-   <span data-ttu-id="61113-112">[**ExecMethod 方法**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="61113-112">[**ExecMethod method**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="61113-113">**ExecQuery 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-113">**ExecQuery method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-execquery)
-   [<span data-ttu-id="61113-114">**Flush 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-114">**Flush method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-flush)
-   [<span data-ttu-id="61113-115">**GetLocalComputerName 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-115">**GetLocalComputerName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalcomputername)
-   [<span data-ttu-id="61113-116">**GetLocalInstancePath 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-116">**GetLocalInstancePath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalinstancepath)
-   [<span data-ttu-id="61113-117">**GetNamespace 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-117">**GetNamespace method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getnamespace)
-   <span data-ttu-id="61113-118">[**GetObject 方法**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span><span class="sxs-lookup"><span data-stu-id="61113-118">[**GetObject method**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span></span>
-   [<span data-ttu-id="61113-119">**GetProviderName 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-119">**GetProviderName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getprovidername)
-   [<span data-ttu-id="61113-120">**MakeLocalPath 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-120">**MakeLocalPath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-makelocalpath)
-   [<span data-ttu-id="61113-121">**提供者方法**</span><span class="sxs-lookup"><span data-stu-id="61113-121">**Provider method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-provider)
-   <span data-ttu-id="61113-122">[**PutInstance 方法**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span><span class="sxs-lookup"><span data-stu-id="61113-122">[**PutInstance method**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span></span>
-   [<span data-ttu-id="61113-123">**SetCreationClassName 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-123">**SetCreationClassName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-setcreationclassname)
-   [<span data-ttu-id="61113-124">**ValidateDeletionFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-124">**ValidateDeletionFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatedeletionflags)
-   [<span data-ttu-id="61113-125">**ValidateEnumerationFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-125">**ValidateEnumerationFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateenumerationflags)
-   [<span data-ttu-id="61113-126">**ValidateFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-126">**ValidateFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateflags)
-   [<span data-ttu-id="61113-127">**ValidateGetObjFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-127">**ValidateGetObjFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validategetobjflags)
-   [<span data-ttu-id="61113-128">**ValidateMethodFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-128">**ValidateMethodFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatemethodflags)
-   [<span data-ttu-id="61113-129">**ValidatePutInstanceFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-129">**ValidatePutInstanceFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateputinstanceflags)
-   [<span data-ttu-id="61113-130">**ValidateQueryFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="61113-130">**ValidateQueryFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatequeryflags)

 

 
