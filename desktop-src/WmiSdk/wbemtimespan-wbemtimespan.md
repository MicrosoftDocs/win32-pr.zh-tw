---
description: WBEMTimeSpan 類別的函式會建立時間範圍物件。 此函式已多載。
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: 'WBEMTimeSpan：： WbemTimeSpan (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: af5724a91ab50b5286e23b3c8095163e415d95e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195221"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a><span data-ttu-id="bbd79-104">WBEMTimeSpan：： WbemTimeSpan 的函式</span><span class="sxs-lookup"><span data-stu-id="bbd79-104">WBEMTimeSpan::WbemTimeSpan constructors</span></span>

<span data-ttu-id="bbd79-105">\[[**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="bbd79-105">\[The [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="bbd79-106">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="bbd79-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="bbd79-107">**WBEMTimeSpan** 類別的函式會建立時間範圍物件。</span><span class="sxs-lookup"><span data-stu-id="bbd79-107">The **WBEMTimeSpan** class constructor creates a time span object.</span></span> <span data-ttu-id="bbd79-108">此函式已多載。</span><span class="sxs-lookup"><span data-stu-id="bbd79-108">The constructor is overloaded.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bbd79-109">多載清單</span><span class="sxs-lookup"><span data-stu-id="bbd79-109">Overload list</span></span>



| <span data-ttu-id="bbd79-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="bbd79-110">Constructor</span></span>                                                                                                 | <span data-ttu-id="bbd79-111">描述</span><span class="sxs-lookup"><span data-stu-id="bbd79-111">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="bbd79-112">[**WBEMTimeSpan ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="bbd79-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                                      | <span data-ttu-id="bbd79-113">建立未初始化的時間範圍物件。</span><span class="sxs-lookup"><span data-stu-id="bbd79-113">Creates an uninitialized time span object.</span></span><br/>                        |
| <span data-ttu-id="bbd79-114">[**WBEMTimeSpan (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="bbd79-114">[**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                               | <span data-ttu-id="bbd79-115">將新的時間範圍物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="bbd79-115">Initializes the new time span object to value in the parameter.</span></span><br/>   |
| <span data-ttu-id="bbd79-116">[**WBEMTimeSpan (int，int，int，int，int，int，int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span><span class="sxs-lookup"><span data-stu-id="bbd79-116">[**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span></span> | <span data-ttu-id="bbd79-117">將新的時間範圍物件初始化為參數中的值。</span><span class="sxs-lookup"><span data-stu-id="bbd79-117">Initializes the new time span object to values in the parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bbd79-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbd79-118">Requirements</span></span>



| <span data-ttu-id="bbd79-119">需求</span><span class="sxs-lookup"><span data-stu-id="bbd79-119">Requirement</span></span> | <span data-ttu-id="bbd79-120">值</span><span class="sxs-lookup"><span data-stu-id="bbd79-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd79-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbd79-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd79-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbd79-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="bbd79-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbd79-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd79-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbd79-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="bbd79-125">標頭</span><span class="sxs-lookup"><span data-stu-id="bbd79-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbd79-126"><dt>WbemTime。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd79-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="bbd79-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bbd79-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbd79-128"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbd79-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="bbd79-129">�</span><span class="sxs-lookup"><span data-stu-id="bbd79-129">�</span></span>

<span data-ttu-id="bbd79-130">�</span><span class="sxs-lookup"><span data-stu-id="bbd79-130">�</span></span>
