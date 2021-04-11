---
description: CInstance：： SetCharSplat 方法會設定字串屬性。
ms.assetid: 7f59a2ea-3513-4a14-ac1a-62ed833d7192
ms.tgt_platform: multiple
title: 'CInstance：： SetCharSplat 方法 (實例 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: e60f24023a9fc704f331d1d071e673720bfdc43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944720"
---
# <a name="cinstancesetcharsplat-methods"></a><span data-ttu-id="4c338-103">CInstance：： SetCharSplat 方法</span><span class="sxs-lookup"><span data-stu-id="4c338-103">CInstance::SetCharSplat methods</span></span>

<span data-ttu-id="4c338-104">\[[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="4c338-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4c338-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="4c338-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4c338-106">**CInstance：： SetCharSplat** 方法會設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="4c338-106">The **CInstance::SetCharSplat** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4c338-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="4c338-107">Overload list</span></span>



| <span data-ttu-id="4c338-108">方法</span><span class="sxs-lookup"><span data-stu-id="4c338-108">Method</span></span>                                                                             | <span data-ttu-id="4c338-109">描述</span><span class="sxs-lookup"><span data-stu-id="4c338-109">Description</span></span>                        |
|:-----------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="4c338-110">[**SetCharSplat (LPCWSTR、DWORD)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_dword))</span><span class="sxs-lookup"><span data-stu-id="4c338-110">[**SetCharSplat(LPCWSTR, DWORD)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_dword))</span></span>     | <span data-ttu-id="4c338-111">設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="4c338-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="4c338-112">[**SetCharSplat (LPCWSTR、LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="4c338-112">[**SetCharSplat(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcstr))</span></span>   | <span data-ttu-id="4c338-113">設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="4c338-113">Sets a string property.</span></span><br/> |
| <span data-ttu-id="4c338-114">[**SetCharSplat (LPCWSTR、LPCWSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="4c338-114">[**SetCharSplat(LPCWSTR, LPCWSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcwstr))</span></span> | <span data-ttu-id="4c338-115">設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="4c338-115">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4c338-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c338-116">Requirements</span></span>



| <span data-ttu-id="4c338-117">需求</span><span class="sxs-lookup"><span data-stu-id="4c338-117">Requirement</span></span> | <span data-ttu-id="4c338-118">值</span><span class="sxs-lookup"><span data-stu-id="4c338-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c338-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c338-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c338-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c338-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4c338-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c338-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c338-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c338-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4c338-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4c338-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c338-124"><dt>實例 .h (包含 FwCommon .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4c338-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4c338-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c338-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c338-126"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c338-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4c338-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4c338-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c338-128"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c338-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c338-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c338-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c338-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="4c338-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

