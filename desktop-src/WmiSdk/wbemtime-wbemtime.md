---
description: WBEMTime 類別的函式可加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'WBEMTime：： WBEMTime (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980703"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="19d17-103">WBEMTime：： WBEMTime 的函式</span><span class="sxs-lookup"><span data-stu-id="19d17-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="19d17-104">\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="19d17-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="19d17-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="19d17-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="19d17-106">**WBEMTime** 類別的函式可加速各種 WINDOWS 和 ANSI C 執行時間時間格式之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="19d17-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="19d17-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="19d17-107">Overload list</span></span>



| <span data-ttu-id="19d17-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="19d17-108">Constructor</span></span>                                                                 | <span data-ttu-id="19d17-109">描述</span><span class="sxs-lookup"><span data-stu-id="19d17-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="19d17-110">[**WBEMTime ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="19d17-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="19d17-111">建立未初始化的時間物件。</span><span class="sxs-lookup"><span data-stu-id="19d17-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="19d17-112">[**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="19d17-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="19d17-113">將新的時間物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="19d17-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="19d17-114">[**WBEMTime (const time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="19d17-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="19d17-115">將新的時間物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="19d17-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="19d17-116">[**WBEMTime (const 結構 tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="19d17-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="19d17-117">將新的時間物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="19d17-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="19d17-118">[**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="19d17-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="19d17-119">將新的時間物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="19d17-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="19d17-120">[**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="19d17-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="19d17-121">將新的時間物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="19d17-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="19d17-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="19d17-122">Requirements</span></span>



| <span data-ttu-id="19d17-123">需求</span><span class="sxs-lookup"><span data-stu-id="19d17-123">Requirement</span></span> | <span data-ttu-id="19d17-124">值</span><span class="sxs-lookup"><span data-stu-id="19d17-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19d17-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19d17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19d17-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19d17-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="19d17-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19d17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19d17-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19d17-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="19d17-129">標頭</span><span class="sxs-lookup"><span data-stu-id="19d17-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="19d17-130"><dt>WbemTime。h</dt></span><span class="sxs-lookup"><span data-stu-id="19d17-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="19d17-131">DLL</span><span class="sxs-lookup"><span data-stu-id="19d17-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d17-132"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d17-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="19d17-133">�</span><span class="sxs-lookup"><span data-stu-id="19d17-133">�</span></span>

<span data-ttu-id="19d17-134">�</span><span class="sxs-lookup"><span data-stu-id="19d17-134">�</span></span>
