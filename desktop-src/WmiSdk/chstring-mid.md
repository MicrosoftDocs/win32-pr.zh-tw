---
description: Mid 方法會從 CHString 字串解壓縮長度 nCount 字元的子字串，從位置 nFirst 開始， (以零為基礎的) 。 方法會傳回已解壓縮之子字串的複本。
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'CHString：： Mid 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989466"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="773e3-104">CHString：： Mid 方法</span><span class="sxs-lookup"><span data-stu-id="773e3-104">CHString::Mid methods</span></span>

<span data-ttu-id="773e3-105">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="773e3-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="773e3-106">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="773e3-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="773e3-107">**Mid** 方法會從 [**CHString**](chstring.md)字串解壓縮長度 *nCount* 字元的子字串，從位置 *nFirst* 開始， (以零為基礎的) 。</span><span class="sxs-lookup"><span data-stu-id="773e3-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="773e3-108">方法會傳回已解壓縮之子字串的複本。</span><span class="sxs-lookup"><span data-stu-id="773e3-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="773e3-109">多載清單</span><span class="sxs-lookup"><span data-stu-id="773e3-109">Overload list</span></span>



| <span data-ttu-id="773e3-110">方法</span><span class="sxs-lookup"><span data-stu-id="773e3-110">Method</span></span>                                        | <span data-ttu-id="773e3-111">描述</span><span class="sxs-lookup"><span data-stu-id="773e3-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="773e3-112">[**Mid (int，int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="773e3-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="773e3-113">解壓縮指定長度和起點的子字串。</span><span class="sxs-lookup"><span data-stu-id="773e3-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="773e3-114">[**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="773e3-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="773e3-115">從 int 開始解壓縮子字串。</span><span class="sxs-lookup"><span data-stu-id="773e3-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="773e3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="773e3-116">Requirements</span></span>



| <span data-ttu-id="773e3-117">需求</span><span class="sxs-lookup"><span data-stu-id="773e3-117">Requirement</span></span> | <span data-ttu-id="773e3-118">值</span><span class="sxs-lookup"><span data-stu-id="773e3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="773e3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="773e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="773e3-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="773e3-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="773e3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="773e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="773e3-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="773e3-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="773e3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="773e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="773e3-124"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="773e3-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="773e3-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="773e3-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="773e3-126"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="773e3-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="773e3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="773e3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="773e3-128"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="773e3-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="773e3-129">�</span><span class="sxs-lookup"><span data-stu-id="773e3-129">�</span></span>

<span data-ttu-id="773e3-130">�</span><span class="sxs-lookup"><span data-stu-id="773e3-130">�</span></span>
