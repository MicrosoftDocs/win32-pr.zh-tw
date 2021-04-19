---
description: Find 方法會在字串中搜尋子字串的第一個相符項。
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'CHString：： Find 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997258"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="39ab4-103">CHString：： Find 方法</span><span class="sxs-lookup"><span data-stu-id="39ab4-103">CHString::Find methods</span></span>

<span data-ttu-id="39ab4-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="39ab4-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="39ab4-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="39ab4-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="39ab4-106">**Find** 方法會在字串中搜尋子字串的第一個相符項。</span><span class="sxs-lookup"><span data-stu-id="39ab4-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="39ab4-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="39ab4-107">Overload list</span></span>



| <span data-ttu-id="39ab4-108">方法</span><span class="sxs-lookup"><span data-stu-id="39ab4-108">Method</span></span>                                          | <span data-ttu-id="39ab4-109">描述</span><span class="sxs-lookup"><span data-stu-id="39ab4-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="39ab4-110">[**尋找 (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="39ab4-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="39ab4-111">搜尋此字串中的 **WSTR** 。</span><span class="sxs-lookup"><span data-stu-id="39ab4-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="39ab4-112">[**尋找 (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="39ab4-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="39ab4-113">搜尋此字串中的 **LPCWSTR** 。</span><span class="sxs-lookup"><span data-stu-id="39ab4-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="39ab4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="39ab4-114">Requirements</span></span>



| <span data-ttu-id="39ab4-115">需求</span><span class="sxs-lookup"><span data-stu-id="39ab4-115">Requirement</span></span> | <span data-ttu-id="39ab4-116">值</span><span class="sxs-lookup"><span data-stu-id="39ab4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ab4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39ab4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39ab4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39ab4-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="39ab4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39ab4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39ab4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39ab4-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="39ab4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="39ab4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ab4-122"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="39ab4-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="39ab4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="39ab4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="39ab4-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="39ab4-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="39ab4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="39ab4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39ab4-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ab4-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="39ab4-127">�</span><span class="sxs-lookup"><span data-stu-id="39ab4-127">�</span></span>

<span data-ttu-id="39ab4-128">�</span><span class="sxs-lookup"><span data-stu-id="39ab4-128">�</span></span>
