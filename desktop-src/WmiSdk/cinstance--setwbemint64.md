---
description: CInstance：： GetWBEMINT64 方法會設定64位整數屬性。
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'CInstance：： SetWBEMINT64 方法 (實例 .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f83e39170125a07f28a25d594ad7203f44750a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944722"
---
# <a name="cinstancesetwbemint64-methods"></a><span data-ttu-id="42a67-103">CInstance：： SetWBEMINT64 方法</span><span class="sxs-lookup"><span data-stu-id="42a67-103">CInstance::SetWBEMINT64 methods</span></span>

<span data-ttu-id="42a67-104">\[[**CInstance**](/windows/win32/api/instance/nl-instance-cinstance)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="42a67-104">\[The [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="42a67-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="42a67-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="42a67-106">[**CInstance：： GetWBEMINT64**](cinstance-getwbemint64.md)方法會設定64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="42a67-106">The [**CInstance::GetWBEMINT64**](cinstance-getwbemint64.md) method sets a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="42a67-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="42a67-107">Overload list</span></span>



| <span data-ttu-id="42a67-108">方法</span><span class="sxs-lookup"><span data-stu-id="42a67-108">Method</span></span>                                                                                               | <span data-ttu-id="42a67-109">描述</span><span class="sxs-lookup"><span data-stu-id="42a67-109">Description</span></span>                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| <span data-ttu-id="42a67-110">[**SetWBEMINT64 (LPCWSTR，const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span><span class="sxs-lookup"><span data-stu-id="42a67-110">[**SetWBEMINT64(LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span></span>    | <span data-ttu-id="42a67-111">設定64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="42a67-111">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="42a67-112">[**SetWBEMINT64 (LPCWSTR，const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="42a67-112">[**SetWBEMINT64(LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span> | <span data-ttu-id="42a67-113">設定64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="42a67-113">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="42a67-114">[**SetWBEMINT64 (LPCWSTR，const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="42a67-114">[**SetWBEMINT64(LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span>  | <span data-ttu-id="42a67-115">設定64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="42a67-115">Sets a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="42a67-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="42a67-116">Requirements</span></span>



| <span data-ttu-id="42a67-117">需求</span><span class="sxs-lookup"><span data-stu-id="42a67-117">Requirement</span></span> | <span data-ttu-id="42a67-118">值</span><span class="sxs-lookup"><span data-stu-id="42a67-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a67-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42a67-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42a67-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42a67-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="42a67-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42a67-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42a67-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42a67-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="42a67-123">標頭</span><span class="sxs-lookup"><span data-stu-id="42a67-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a67-124"><dt>實例 .h (包含 FwCommon .h) </dt></span><span class="sxs-lookup"><span data-stu-id="42a67-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="42a67-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="42a67-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="42a67-126"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42a67-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="42a67-127">DLL</span><span class="sxs-lookup"><span data-stu-id="42a67-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a67-128"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a67-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a67-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42a67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a67-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="42a67-130">**CInstance**</span></span>](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

<span data-ttu-id="42a67-131">�</span><span class="sxs-lookup"><span data-stu-id="42a67-131">�</span></span>

<span data-ttu-id="42a67-132">�</span><span class="sxs-lookup"><span data-stu-id="42a67-132">�</span></span>
