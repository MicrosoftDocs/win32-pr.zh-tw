---
description: WBEMTime 類別指派運算子會進行多載，以加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。 不同的多載簽章如下所示。
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'WBEMTime：： operator = 運算子 (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320820"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="33b13-104">WBEMTime：： operator = 運算子</span><span class="sxs-lookup"><span data-stu-id="33b13-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="33b13-105">\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="33b13-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="33b13-106">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="33b13-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="33b13-107">[**WBEMTime**](wbemtime.md)類別指派運算子會進行多載，以加速各種 WINDOWS 和 ANSI C 執行時間時間格式之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="33b13-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="33b13-108">不同的多載簽章如下所示。</span><span class="sxs-lookup"><span data-stu-id="33b13-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="33b13-109">多載清單</span><span class="sxs-lookup"><span data-stu-id="33b13-109">Overload list</span></span>



| <span data-ttu-id="33b13-110">運算子</span><span class="sxs-lookup"><span data-stu-id="33b13-110">Operator</span></span>                                                                     | <span data-ttu-id="33b13-111">描述</span><span class="sxs-lookup"><span data-stu-id="33b13-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="33b13-112">[**operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="33b13-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="33b13-113">將 **BSTR** 轉換成 **WBEMTime** 格式。</span><span class="sxs-lookup"><span data-stu-id="33b13-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="33b13-114">[**operator = (時間 \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="33b13-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="33b13-115">將 **時間 \_ t** 轉換成 **WBEMTime** 格式。</span><span class="sxs-lookup"><span data-stu-id="33b13-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="33b13-116">[**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="33b13-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="33b13-117">將 **FILETIME** 轉換成 **WBEMTime** 格式。</span><span class="sxs-lookup"><span data-stu-id="33b13-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="33b13-118">[**operator = (結構 tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="33b13-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="33b13-119">將 **tm** 結構轉換為 **WBEMTime** 格式。</span><span class="sxs-lookup"><span data-stu-id="33b13-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="33b13-120">[**operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="33b13-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="33b13-121">將 **SYSTEMTIME** 轉換為 **WBEMTime** 格式。</span><span class="sxs-lookup"><span data-stu-id="33b13-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="33b13-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="33b13-122">Requirements</span></span>



| <span data-ttu-id="33b13-123">需求</span><span class="sxs-lookup"><span data-stu-id="33b13-123">Requirement</span></span> | <span data-ttu-id="33b13-124">值</span><span class="sxs-lookup"><span data-stu-id="33b13-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b13-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33b13-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33b13-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33b13-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="33b13-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33b13-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33b13-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33b13-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="33b13-129">標頭</span><span class="sxs-lookup"><span data-stu-id="33b13-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="33b13-130"><dt>WbemTime。h</dt></span><span class="sxs-lookup"><span data-stu-id="33b13-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="33b13-131">DLL</span><span class="sxs-lookup"><span data-stu-id="33b13-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33b13-132"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b13-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="33b13-133">�</span><span class="sxs-lookup"><span data-stu-id="33b13-133">�</span></span>

<span data-ttu-id="33b13-134">�</span><span class="sxs-lookup"><span data-stu-id="33b13-134">�</span></span>
