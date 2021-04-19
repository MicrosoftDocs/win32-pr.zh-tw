---
description: 多載的 FormatMessageW 方法會將訊息字串格式化。
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'CHString：： FormatMessageW 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980897"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="28dc2-103">CHString：： FormatMessageW 方法</span><span class="sxs-lookup"><span data-stu-id="28dc2-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="28dc2-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="28dc2-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="28dc2-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="28dc2-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="28dc2-106">多載的 **FormatMessageW** 方法會將訊息字串格式化。</span><span class="sxs-lookup"><span data-stu-id="28dc2-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="28dc2-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="28dc2-107">Overload list</span></span>



| <span data-ttu-id="28dc2-108">方法</span><span class="sxs-lookup"><span data-stu-id="28dc2-108">Method</span></span>                                                              | <span data-ttu-id="28dc2-109">描述</span><span class="sxs-lookup"><span data-stu-id="28dc2-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28dc2-110">[**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28dc2-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="28dc2-111">根據 **UINT** 指定的資源識別碼來格式化此訊息。</span><span class="sxs-lookup"><span data-stu-id="28dc2-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="28dc2-112">[**FormatMessageW (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="28dc2-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="28dc2-113">根據 **LPCWSTR** 所指定的格式來格式化此訊息字串。</span><span class="sxs-lookup"><span data-stu-id="28dc2-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="28dc2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="28dc2-114">Requirements</span></span>



| <span data-ttu-id="28dc2-115">需求</span><span class="sxs-lookup"><span data-stu-id="28dc2-115">Requirement</span></span> | <span data-ttu-id="28dc2-116">值</span><span class="sxs-lookup"><span data-stu-id="28dc2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28dc2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28dc2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28dc2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28dc2-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="28dc2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28dc2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28dc2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28dc2-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="28dc2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="28dc2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="28dc2-122"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="28dc2-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="28dc2-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="28dc2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="28dc2-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28dc2-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="28dc2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="28dc2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28dc2-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28dc2-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="28dc2-127">�</span><span class="sxs-lookup"><span data-stu-id="28dc2-127">�</span></span>

<span data-ttu-id="28dc2-128">�</span><span class="sxs-lookup"><span data-stu-id="28dc2-128">�</span></span>
