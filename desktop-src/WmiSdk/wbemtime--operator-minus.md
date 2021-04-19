---
description: WBEMTime 類別減法運算子 (&\# 8211; ) 已多載至：
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'WBEMTime：： operator-運算子 (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983912"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="f5d3b-103">WBEMTime：： operator-運算子</span><span class="sxs-lookup"><span data-stu-id="f5d3b-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="f5d3b-104">\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="f5d3b-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f5d3b-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="f5d3b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f5d3b-106">[**WBEMTime**](wbemtime.md)類別減法運算子 () 已多載至：</span><span class="sxs-lookup"><span data-stu-id="f5d3b-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="f5d3b-107">從物件的時間減去時間範圍，以產生包含所產生時間的新時間物件。</span><span class="sxs-lookup"><span data-stu-id="f5d3b-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="f5d3b-108">從物件的時間減去時間，以產生新的時間範圍物件，其中包含兩次之間的差異。</span><span class="sxs-lookup"><span data-stu-id="f5d3b-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f5d3b-109">多載清單</span><span class="sxs-lookup"><span data-stu-id="f5d3b-109">Overload list</span></span>



| <span data-ttu-id="f5d3b-110">運算子</span><span class="sxs-lookup"><span data-stu-id="f5d3b-110">Operator</span></span>                                                                         | <span data-ttu-id="f5d3b-111">描述</span><span class="sxs-lookup"><span data-stu-id="f5d3b-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="f5d3b-112">**operator- (WBEMTime&)**</span><span class="sxs-lookup"><span data-stu-id="f5d3b-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="f5d3b-113">從 **WBEMTime** 減去 **WBEMTime** 。</span><span class="sxs-lookup"><span data-stu-id="f5d3b-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="f5d3b-114">[**operator- (WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="f5d3b-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="f5d3b-115">從 **WBEMTime** 減去 [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) 。</span><span class="sxs-lookup"><span data-stu-id="f5d3b-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f5d3b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5d3b-116">Requirements</span></span>



| <span data-ttu-id="f5d3b-117">需求</span><span class="sxs-lookup"><span data-stu-id="f5d3b-117">Requirement</span></span> | <span data-ttu-id="f5d3b-118">值</span><span class="sxs-lookup"><span data-stu-id="f5d3b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d3b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5d3b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d3b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5d3b-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f5d3b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5d3b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d3b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5d3b-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f5d3b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f5d3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d3b-124"><dt>WbemTime。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d3b-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="f5d3b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f5d3b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d3b-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d3b-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="f5d3b-127">�</span><span class="sxs-lookup"><span data-stu-id="f5d3b-127">�</span></span>

<span data-ttu-id="f5d3b-128">�</span><span class="sxs-lookup"><span data-stu-id="f5d3b-128">�</span></span>
