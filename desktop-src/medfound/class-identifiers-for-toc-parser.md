---
description: 下列類別會在 wmcodecdsp 中宣告並與類別識別碼關聯 (Clsid) 。
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: '目錄剖析器的類別識別碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971155"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="b2df6-103">目錄剖析器的類別識別碼</span><span class="sxs-lookup"><span data-stu-id="b2df6-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="b2df6-104">下列類別會在 wmcodecdsp 中宣告並與類別識別碼關聯 (Clsid) 。</span><span class="sxs-lookup"><span data-stu-id="b2df6-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="b2df6-105">類別名稱</span><span class="sxs-lookup"><span data-stu-id="b2df6-105">Class name</span></span>       | <span data-ttu-id="b2df6-106">易記的物件名稱</span><span class="sxs-lookup"><span data-stu-id="b2df6-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="b2df6-107">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="b2df6-107">CTocEntry</span></span>        | <span data-ttu-id="b2df6-108">TOC 專案</span><span class="sxs-lookup"><span data-stu-id="b2df6-108">TOC Entry</span></span>            |
| <span data-ttu-id="b2df6-109">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="b2df6-109">CTocEntryList</span></span>    | <span data-ttu-id="b2df6-110">目錄專案清單</span><span class="sxs-lookup"><span data-stu-id="b2df6-110">TOC Entry List</span></span>       |
| <span data-ttu-id="b2df6-111">CToc</span><span class="sxs-lookup"><span data-stu-id="b2df6-111">CToc</span></span>             | <span data-ttu-id="b2df6-112">目錄</span><span class="sxs-lookup"><span data-stu-id="b2df6-112">TOC</span></span>                  |
| <span data-ttu-id="b2df6-113">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="b2df6-113">CTocCollection</span></span>   | <span data-ttu-id="b2df6-114">目錄集合</span><span class="sxs-lookup"><span data-stu-id="b2df6-114">TOC Collection</span></span>       |
| <span data-ttu-id="b2df6-115">CTocParser</span><span class="sxs-lookup"><span data-stu-id="b2df6-115">CTocParser</span></span>       | <span data-ttu-id="b2df6-116">TOC 剖析器</span><span class="sxs-lookup"><span data-stu-id="b2df6-116">TOC Parser</span></span>           |
| <span data-ttu-id="b2df6-117">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="b2df6-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="b2df6-118">TOC 產生器</span><span class="sxs-lookup"><span data-stu-id="b2df6-118">TOC Generator</span></span>        |



 

<span data-ttu-id="b2df6-119">上表為每個類別提供易記的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="b2df6-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="b2df6-120">本檔使用這些易記名稱來參考類別的實例。</span><span class="sxs-lookup"><span data-stu-id="b2df6-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="b2df6-121">例如，檔是指 CTocEntry 類別的實例做為 TOC 專案物件。</span><span class="sxs-lookup"><span data-stu-id="b2df6-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="b2df6-122">在程式碼中，您可以使用 **\_ \_ uuidof** 來參考 clsid。</span><span class="sxs-lookup"><span data-stu-id="b2df6-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="b2df6-123">例如，您可以使用下列程式碼來參考 CTocGeneratorDmo 的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b2df6-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="b2df6-124">Wmcodecdsp 中定義的 CLSID 常數</span><span class="sxs-lookup"><span data-stu-id="b2df6-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="b2df6-125">除了使用 **\_ \_ uuidof** 之外，您還可以使用常數來參考 clsid。</span><span class="sxs-lookup"><span data-stu-id="b2df6-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="b2df6-126">下列常數定義于 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="b2df6-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="b2df6-127">類別名稱</span><span class="sxs-lookup"><span data-stu-id="b2df6-127">Class name</span></span>     | <span data-ttu-id="b2df6-128">CLSID 常數</span><span class="sxs-lookup"><span data-stu-id="b2df6-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="b2df6-129">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="b2df6-129">CTocEntry</span></span>      | <span data-ttu-id="b2df6-130">CLSID \_ CTocEntry</span><span class="sxs-lookup"><span data-stu-id="b2df6-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="b2df6-131">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="b2df6-131">CTocEntryList</span></span>  | <span data-ttu-id="b2df6-132">CLSID \_ CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="b2df6-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="b2df6-133">CToc</span><span class="sxs-lookup"><span data-stu-id="b2df6-133">CToc</span></span>           | <span data-ttu-id="b2df6-134">CLSID \_ CToc</span><span class="sxs-lookup"><span data-stu-id="b2df6-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="b2df6-135">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="b2df6-135">CTocCollection</span></span> | <span data-ttu-id="b2df6-136">CLSID \_ CTocCollection</span><span class="sxs-lookup"><span data-stu-id="b2df6-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="b2df6-137">CTocParser</span><span class="sxs-lookup"><span data-stu-id="b2df6-137">CTocParser</span></span>     | <span data-ttu-id="b2df6-138">CLSID \_ CTocParser</span><span class="sxs-lookup"><span data-stu-id="b2df6-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="b2df6-139">Wmcodecdspuuid 中定義的 CLSID 常數</span><span class="sxs-lookup"><span data-stu-id="b2df6-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="b2df6-140">下列 CLSID 常數是在 wmcodecdsp 中宣告，但未定義。</span><span class="sxs-lookup"><span data-stu-id="b2df6-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="b2df6-141">若要在程式碼中使用它，您必須連結至 wmcodecdspuuid .lib。</span><span class="sxs-lookup"><span data-stu-id="b2df6-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="b2df6-142">類別名稱</span><span class="sxs-lookup"><span data-stu-id="b2df6-142">Class name</span></span>       | <span data-ttu-id="b2df6-143">CLSID 常數</span><span class="sxs-lookup"><span data-stu-id="b2df6-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="b2df6-144">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="b2df6-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="b2df6-145">CLSID \_ CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="b2df6-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b2df6-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2df6-146">Requirements</span></span>



| <span data-ttu-id="b2df6-147">需求</span><span class="sxs-lookup"><span data-stu-id="b2df6-147">Requirement</span></span> | <span data-ttu-id="b2df6-148">值</span><span class="sxs-lookup"><span data-stu-id="b2df6-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2df6-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2df6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b2df6-150">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2df6-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2df6-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2df6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b2df6-152">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2df6-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2df6-153">標頭</span><span class="sxs-lookup"><span data-stu-id="b2df6-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2df6-154"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2df6-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b2df6-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b2df6-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2df6-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2df6-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b2df6-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2df6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2df6-158">目錄剖析器物件</span><span class="sxs-lookup"><span data-stu-id="b2df6-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




