---
description: GetEmptyInstance 方法會捕獲指定類別的單一擴展實例。
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'CWbemProviderGlue：： GetEmptyInstance 方法 (WbemGlue .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983567"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="14555-103">CWbemProviderGlue：： GetEmptyInstance 方法</span><span class="sxs-lookup"><span data-stu-id="14555-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="14555-104">\[[**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="14555-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="14555-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="14555-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="14555-106">**GetEmptyInstance** 方法會捕獲指定類別的單一擴展實例。</span><span class="sxs-lookup"><span data-stu-id="14555-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="14555-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="14555-107">Overload list</span></span>



| <span data-ttu-id="14555-108">方法</span><span class="sxs-lookup"><span data-stu-id="14555-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="14555-109">描述</span><span class="sxs-lookup"><span data-stu-id="14555-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="14555-110">[**GetEmptyInstance (LPCWSTR、CInstance、LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="14555-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="14555-111">抓取指定類別的單一擴展實例。</span><span class="sxs-lookup"><span data-stu-id="14555-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="14555-112">[**GetEmptyInstance (MethodCoNtext、LPCWSTR、CInstance、LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="14555-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="14555-113">抓取指定類別的單一擴展實例。</span><span class="sxs-lookup"><span data-stu-id="14555-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="14555-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="14555-114">Requirements</span></span>



| <span data-ttu-id="14555-115">需求</span><span class="sxs-lookup"><span data-stu-id="14555-115">Requirement</span></span> | <span data-ttu-id="14555-116">值</span><span class="sxs-lookup"><span data-stu-id="14555-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14555-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14555-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14555-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14555-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="14555-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14555-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14555-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14555-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="14555-121">標頭</span><span class="sxs-lookup"><span data-stu-id="14555-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14555-122"><dt>WbemGlue (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="14555-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="14555-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="14555-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="14555-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="14555-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="14555-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14555-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14555-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14555-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="14555-127">�</span><span class="sxs-lookup"><span data-stu-id="14555-127">�</span></span>

<span data-ttu-id="14555-128">�</span><span class="sxs-lookup"><span data-stu-id="14555-128">�</span></span>
