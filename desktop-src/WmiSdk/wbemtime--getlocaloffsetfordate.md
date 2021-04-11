---
description: GetLocalOffsetForDate 方法會傳回以分鐘為單位的位移 (+ 或 &\# 8211; 在引數中提供的時間內，) GMT 和本地時間之間的位移。
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'WBEMTime：： GetLocalOffsetForDate 方法 (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850744"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="83e55-103">WBEMTime：： GetLocalOffsetForDate 方法</span><span class="sxs-lookup"><span data-stu-id="83e55-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="83e55-104">\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="83e55-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="83e55-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="83e55-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="83e55-106">**GetLocalOffsetForDate** 方法會傳回引數中所提供時間的時差（以分鐘為單位） (+ 或) 之間的時差和本地時間。</span><span class="sxs-lookup"><span data-stu-id="83e55-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="83e55-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="83e55-107">Overload list</span></span>



| <span data-ttu-id="83e55-108">方法</span><span class="sxs-lookup"><span data-stu-id="83e55-108">Method</span></span>                                                                                           | <span data-ttu-id="83e55-109">描述</span><span class="sxs-lookup"><span data-stu-id="83e55-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="83e55-110">[**GetLocalOffsetForDate (time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="83e55-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="83e55-111">引數是 **時間 \_ t** 的參考。</span><span class="sxs-lookup"><span data-stu-id="83e55-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="83e55-112">[**GetLocalOffsetForDate (FILETIME \*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="83e55-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="83e55-113">引數是 **FILETIME** 的指標。</span><span class="sxs-lookup"><span data-stu-id="83e55-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="83e55-114">**GetLocalOffsetForDate (結構 tm \*)**</span><span class="sxs-lookup"><span data-stu-id="83e55-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="83e55-115">引數是 **tm** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="83e55-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="83e55-116">[**GetLocalOffsetForDate (SYSTEMTIME \*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="83e55-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="83e55-117">引數是指向 **SYSTEMTIME** 的指標。</span><span class="sxs-lookup"><span data-stu-id="83e55-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="83e55-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="83e55-118">Requirements</span></span>



| <span data-ttu-id="83e55-119">需求</span><span class="sxs-lookup"><span data-stu-id="83e55-119">Requirement</span></span> | <span data-ttu-id="83e55-120">值</span><span class="sxs-lookup"><span data-stu-id="83e55-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e55-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83e55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83e55-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83e55-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="83e55-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83e55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83e55-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83e55-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="83e55-125">標頭</span><span class="sxs-lookup"><span data-stu-id="83e55-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="83e55-126"><dt>WbemTime。h</dt></span><span class="sxs-lookup"><span data-stu-id="83e55-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="83e55-127">DLL</span><span class="sxs-lookup"><span data-stu-id="83e55-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83e55-128"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83e55-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="83e55-129">�</span><span class="sxs-lookup"><span data-stu-id="83e55-129">�</span></span>

<span data-ttu-id="83e55-130">�</span><span class="sxs-lookup"><span data-stu-id="83e55-130">�</span></span>
