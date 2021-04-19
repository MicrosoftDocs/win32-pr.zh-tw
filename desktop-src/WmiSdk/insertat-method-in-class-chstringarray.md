---
description: InsertAt 方法會將元素 (或多個元素) 或指定的索引處之其他陣列的所有元素插入。
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'CHStringArray：： InsertAt 方法 (ChStrArr .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980705"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="1fb9e-103">CHStringArray：： InsertAt 方法</span><span class="sxs-lookup"><span data-stu-id="1fb9e-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="1fb9e-104">\[[**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="1fb9e-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1fb9e-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="1fb9e-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1fb9e-106">**InsertAt** 方法會將元素 (或多個元素) 或指定的索引處之其他陣列的所有元素插入。</span><span class="sxs-lookup"><span data-stu-id="1fb9e-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1fb9e-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="1fb9e-107">Overload list</span></span>



| <span data-ttu-id="1fb9e-108">方法</span><span class="sxs-lookup"><span data-stu-id="1fb9e-108">Method</span></span>                                                                               | <span data-ttu-id="1fb9e-109">描述</span><span class="sxs-lookup"><span data-stu-id="1fb9e-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb9e-110">[**InsertAt (int，LPCWSTR，int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1fb9e-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="1fb9e-111">在陣列中的指定索引處插入一或多個元素。</span><span class="sxs-lookup"><span data-stu-id="1fb9e-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="1fb9e-112">[**InsertAt (int，CHStringArray \*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="1fb9e-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="1fb9e-113">將另一個 [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) 的所有元素插入陣列中的指定索引處。</span><span class="sxs-lookup"><span data-stu-id="1fb9e-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1fb9e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fb9e-114">Requirements</span></span>



| <span data-ttu-id="1fb9e-115">需求</span><span class="sxs-lookup"><span data-stu-id="1fb9e-115">Requirement</span></span> | <span data-ttu-id="1fb9e-116">值</span><span class="sxs-lookup"><span data-stu-id="1fb9e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb9e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fb9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb9e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fb9e-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1fb9e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fb9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb9e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fb9e-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1fb9e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1fb9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fb9e-122"><dt>ChStrArr (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="1fb9e-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1fb9e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="1fb9e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fb9e-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fb9e-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="1fb9e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb9e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fb9e-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fb9e-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb9e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fb9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb9e-128">**CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="1fb9e-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="1fb9e-129">�</span><span class="sxs-lookup"><span data-stu-id="1fb9e-129">�</span></span>

<span data-ttu-id="1fb9e-130">�</span><span class="sxs-lookup"><span data-stu-id="1fb9e-130">�</span></span>
