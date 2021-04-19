---
description: 這些注標運算子會設定或取得指定索引處的元素。 這些運算子可方便替代 SetAt 和 GetAt 方法。
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray：： operator [] (ChStrArr .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987337"
---
# <a name="chstringarrayoperator--"></a><span data-ttu-id="4150e-104">CHStringArray：： operator \[\]</span><span class="sxs-lookup"><span data-stu-id="4150e-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="4150e-105">\[[**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="4150e-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4150e-106">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="4150e-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4150e-107">這些注標運算子會設定或取得指定索引處的元素。</span><span class="sxs-lookup"><span data-stu-id="4150e-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="4150e-108">這些運算子可方便替代 [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) 和 [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) 方法。</span><span class="sxs-lookup"><span data-stu-id="4150e-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="4150e-109">參數</span><span class="sxs-lookup"><span data-stu-id="4150e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4150e-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span><span class="sxs-lookup"><span data-stu-id="4150e-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="4150e-111">大於或等於零且小於或等於 System.array.getupperbound 所傳回值的整數索引。 [ ](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="4150e-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="4150e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4150e-112">Return Values</span></span>

<span data-ttu-id="4150e-113">注標運算子會傳回目前位於此索引的 [**CHString**](chstring.md) 指標元素。</span><span class="sxs-lookup"><span data-stu-id="4150e-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="4150e-114">備註</span><span class="sxs-lookup"><span data-stu-id="4150e-114">Remarks</span></span>

<span data-ttu-id="4150e-115">您可以使用第一個運算子來呼叫不是 **const** 的陣列、右邊的 (r-值) 或左邊 (左值) 指派語句的側邊。</span><span class="sxs-lookup"><span data-stu-id="4150e-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="4150e-116">第二個（呼叫 **const** 陣列）只能用在右邊。</span><span class="sxs-lookup"><span data-stu-id="4150e-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="4150e-117">如果在指派) 語句的左側或右側 (的注標是否超出範圍，就會判斷提示程式庫的偵錯工具版本。</span><span class="sxs-lookup"><span data-stu-id="4150e-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="4150e-118">範例</span><span class="sxs-lookup"><span data-stu-id="4150e-118">Examples</span></span>

<span data-ttu-id="4150e-119">下列程式碼範例示範如何使用 [**CHStringArray：： operator \[ \]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4150e-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a><span data-ttu-id="4150e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4150e-120">Requirements</span></span>



| <span data-ttu-id="4150e-121">需求</span><span class="sxs-lookup"><span data-stu-id="4150e-121">Requirement</span></span> | <span data-ttu-id="4150e-122">值</span><span class="sxs-lookup"><span data-stu-id="4150e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4150e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4150e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4150e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4150e-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4150e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4150e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4150e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4150e-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4150e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4150e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4150e-128"><dt>ChStrArr (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="4150e-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4150e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="4150e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4150e-130"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4150e-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4150e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4150e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4150e-132"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4150e-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4150e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4150e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4150e-134">**CHStringArray：： Add**</span><span class="sxs-lookup"><span data-stu-id="4150e-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="4150e-135">[**CHStringArray：： GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="4150e-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="4150e-136">[**CHStringArray：： SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="4150e-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

