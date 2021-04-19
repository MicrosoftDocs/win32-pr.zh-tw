---
description: CInstance：： SetCHString 方法會設定字串屬性。
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'CInstance：： SetCHString 方法 (實例 .h) '
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
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983788"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="be4af-103">CInstance：： SetCHString 方法</span><span class="sxs-lookup"><span data-stu-id="be4af-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="be4af-104">\[[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="be4af-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="be4af-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="be4af-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="be4af-106">**CInstance：： SetCHString** 方法會設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="be4af-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="be4af-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="be4af-107">Overload list</span></span>



| <span data-ttu-id="be4af-108">方法</span><span class="sxs-lookup"><span data-stu-id="be4af-108">Method</span></span>                                                                                           | <span data-ttu-id="be4af-109">描述</span><span class="sxs-lookup"><span data-stu-id="be4af-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="be4af-110">[**SetCHString (LPCWSTR、LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="be4af-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="be4af-111">設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="be4af-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="be4af-112">[**SetCHString (LPCWSTR，const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="be4af-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="be4af-113">設定字串屬性。</span><span class="sxs-lookup"><span data-stu-id="be4af-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="be4af-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="be4af-114">Requirements</span></span>



| <span data-ttu-id="be4af-115">需求</span><span class="sxs-lookup"><span data-stu-id="be4af-115">Requirement</span></span> | <span data-ttu-id="be4af-116">值</span><span class="sxs-lookup"><span data-stu-id="be4af-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4af-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be4af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be4af-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be4af-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="be4af-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be4af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="be4af-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be4af-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="be4af-121">標頭</span><span class="sxs-lookup"><span data-stu-id="be4af-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="be4af-122"><dt>實例 .h (包含 FwCommon .h) </dt></span><span class="sxs-lookup"><span data-stu-id="be4af-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="be4af-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="be4af-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="be4af-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be4af-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="be4af-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be4af-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be4af-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be4af-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4af-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be4af-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4af-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="be4af-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

