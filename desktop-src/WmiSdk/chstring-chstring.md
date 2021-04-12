---
description: 下列每個函式都會使用指定的資料來初始化新的 CHString 物件。
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'CHString：： CHString (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193064"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="2acae-103">CHString：： CHString 的函式</span><span class="sxs-lookup"><span data-stu-id="2acae-103">CHString::CHString constructors</span></span>

<span data-ttu-id="2acae-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="2acae-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="2acae-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="2acae-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="2acae-106">下列每個函式都會使用指定的資料來初始化新的 [**CHString**](chstring.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2acae-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2acae-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="2acae-107">Overload list</span></span>



| <span data-ttu-id="2acae-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="2acae-108">Constructor</span></span>                                                                        | <span data-ttu-id="2acae-109">描述</span><span class="sxs-lookup"><span data-stu-id="2acae-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="2acae-110">**CHString ()**</span><span class="sxs-lookup"><span data-stu-id="2acae-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="2acae-111">建立空的 CHString 物件。</span><span class="sxs-lookup"><span data-stu-id="2acae-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="2acae-112">[**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="2acae-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="2acae-113">使用 LPCSTR 值初始化。</span><span class="sxs-lookup"><span data-stu-id="2acae-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="2acae-114">[**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="2acae-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="2acae-115">使用 LPCWSTR 值初始化。</span><span class="sxs-lookup"><span data-stu-id="2acae-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="2acae-116">[**CHString (WCHAR，int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="2acae-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="2acae-117">使用 WCHAR 值的 int 複本進行初始化。</span><span class="sxs-lookup"><span data-stu-id="2acae-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="2acae-118">[**CHString (LPCWSTR，int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="2acae-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="2acae-119">使用 LPCWSTR 值的 int 複本進行初始化。</span><span class="sxs-lookup"><span data-stu-id="2acae-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="2acae-120">[**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="2acae-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="2acae-121">複寫 CHString 參數。</span><span class="sxs-lookup"><span data-stu-id="2acae-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="2acae-122">[**CHString (const 不帶正負號的 char \*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="2acae-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="2acae-123">使用 char 所指向的值進行初始化 \* 。</span><span class="sxs-lookup"><span data-stu-id="2acae-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="2acae-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2acae-124">Requirements</span></span>



| <span data-ttu-id="2acae-125">需求</span><span class="sxs-lookup"><span data-stu-id="2acae-125">Requirement</span></span> | <span data-ttu-id="2acae-126">值</span><span class="sxs-lookup"><span data-stu-id="2acae-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acae-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2acae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2acae-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2acae-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="2acae-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2acae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2acae-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2acae-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="2acae-131">標頭</span><span class="sxs-lookup"><span data-stu-id="2acae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2acae-132"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="2acae-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2acae-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="2acae-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2acae-134"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2acae-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="2acae-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2acae-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2acae-136"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2acae-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="2acae-137">�</span><span class="sxs-lookup"><span data-stu-id="2acae-137">�</span></span>

<span data-ttu-id="2acae-138">�</span><span class="sxs-lookup"><span data-stu-id="2acae-138">�</span></span>
