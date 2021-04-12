---
description: CInstance：： GetWBEMINT64 方法會捕獲64位整數屬性。
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'CInstance：： GetWBEMINT64 方法 (實例 .h) '
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
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319687"
---
# <a name="cinstancegetwbemint64-methods"></a><span data-ttu-id="4bcf5-103">CInstance：： GetWBEMINT64 方法</span><span class="sxs-lookup"><span data-stu-id="4bcf5-103">CInstance::GetWBEMINT64 methods</span></span>

<span data-ttu-id="4bcf5-104">\[[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="4bcf5-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4bcf5-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="4bcf5-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4bcf5-106">**CInstance：： GetWBEMINT64** 方法會捕獲64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="4bcf5-106">The **CInstance::GetWBEMINT64** method retrieves a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4bcf5-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="4bcf5-107">Overload list</span></span>



| <span data-ttu-id="4bcf5-108">方法</span><span class="sxs-lookup"><span data-stu-id="4bcf5-108">Method</span></span>                                                                                   | <span data-ttu-id="4bcf5-109">描述</span><span class="sxs-lookup"><span data-stu-id="4bcf5-109">Description</span></span>                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| <span data-ttu-id="4bcf5-110">[**GetWBEMINT64 (LPCWSTR、LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span><span class="sxs-lookup"><span data-stu-id="4bcf5-110">[**GetWBEMINT64(LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span></span>   | <span data-ttu-id="4bcf5-111">捕獲64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="4bcf5-111">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="4bcf5-112">[**GetWBEMINT64 (LPCWSTR、WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="4bcf5-112">[**GetWBEMINT64(LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="4bcf5-113">捕獲64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="4bcf5-113">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="4bcf5-114">[**GetWBEMINT64 (LPCWSTR、ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="4bcf5-114">[**GetWBEMINT64(LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="4bcf5-115">捕獲64位整數屬性。</span><span class="sxs-lookup"><span data-stu-id="4bcf5-115">Retrieves a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4bcf5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bcf5-116">Requirements</span></span>



| <span data-ttu-id="4bcf5-117">需求</span><span class="sxs-lookup"><span data-stu-id="4bcf5-117">Requirement</span></span> | <span data-ttu-id="4bcf5-118">值</span><span class="sxs-lookup"><span data-stu-id="4bcf5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcf5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bcf5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcf5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bcf5-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4bcf5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bcf5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcf5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bcf5-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4bcf5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4bcf5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bcf5-124"><dt>實例 .h (包含 FwCommon .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4bcf5-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4bcf5-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bcf5-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bcf5-126"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf5-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4bcf5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4bcf5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bcf5-128"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf5-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcf5-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bcf5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcf5-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="4bcf5-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

