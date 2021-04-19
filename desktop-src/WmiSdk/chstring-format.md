---
description: Format 方法會格式化並將一連串的字元和值儲存在 CHString 字串中。
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'CHString：： Format 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976938"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="0beda-103">CHString：： Format 方法</span><span class="sxs-lookup"><span data-stu-id="0beda-103">CHString::Format methods</span></span>

<span data-ttu-id="0beda-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="0beda-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0beda-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="0beda-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0beda-106">**Format** 方法會格式化並將一連串的字元和值儲存在 [**CHString**](chstring.md)字串中。</span><span class="sxs-lookup"><span data-stu-id="0beda-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0beda-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="0beda-107">Overload list</span></span>



| <span data-ttu-id="0beda-108">方法</span><span class="sxs-lookup"><span data-stu-id="0beda-108">Method</span></span>                                              | <span data-ttu-id="0beda-109">描述</span><span class="sxs-lookup"><span data-stu-id="0beda-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0beda-110">[**格式 (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0beda-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="0beda-111">根據 **UINT** 所指定的資源識別碼，將此 CHString 格式化。</span><span class="sxs-lookup"><span data-stu-id="0beda-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="0beda-112">[**(LPCWSTR 格式的格式)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="0beda-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="0beda-113">根據 **LPCWSTR** 所指定的格式，將這個 CHString 格式化。</span><span class="sxs-lookup"><span data-stu-id="0beda-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="0beda-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0beda-114">Requirements</span></span>



| <span data-ttu-id="0beda-115">需求</span><span class="sxs-lookup"><span data-stu-id="0beda-115">Requirement</span></span> | <span data-ttu-id="0beda-116">值</span><span class="sxs-lookup"><span data-stu-id="0beda-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0beda-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0beda-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0beda-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0beda-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0beda-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0beda-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0beda-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0beda-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0beda-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0beda-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0beda-122"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="0beda-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0beda-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="0beda-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0beda-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0beda-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="0beda-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0beda-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0beda-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0beda-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="0beda-127">�</span><span class="sxs-lookup"><span data-stu-id="0beda-127">�</span></span>

<span data-ttu-id="0beda-128">�</span><span class="sxs-lookup"><span data-stu-id="0beda-128">�</span></span>
