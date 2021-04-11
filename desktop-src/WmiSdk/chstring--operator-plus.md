---
description: + 串連運算子會聯結兩個字串，並傳回 CHString 物件。
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString：： operator + (ChString .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694120"
---
# <a name="chstringoperator"></a><span data-ttu-id="ceb23-103">CHString：： operator +</span><span class="sxs-lookup"><span data-stu-id="ceb23-103">CHString::operator+</span></span>

<span data-ttu-id="ceb23-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="ceb23-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ceb23-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="ceb23-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ceb23-106">+ 串連運算子會聯結兩個字串，並傳回 [**CHString**](chstring.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ceb23-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="ceb23-107">參數</span><span class="sxs-lookup"><span data-stu-id="ceb23-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb23-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str、str1、str2*</span><span class="sxs-lookup"><span data-stu-id="ceb23-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="ceb23-109">串連的 [**CHString**](chstring.md)字串。</span><span class="sxs-lookup"><span data-stu-id="ceb23-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="ceb23-110"><span id="ch"></span><span id="CH"></span>*>ch*</span><span class="sxs-lookup"><span data-stu-id="ceb23-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="ceb23-111">串連至字串或串連為字元之字串的字元。</span><span class="sxs-lookup"><span data-stu-id="ceb23-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="ceb23-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="ceb23-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="ceb23-113">以 **Null** 結束的字元字串指標。</span><span class="sxs-lookup"><span data-stu-id="ceb23-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="ceb23-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ceb23-114">Return Values</span></span>

<span data-ttu-id="ceb23-115">此串連運算子會傳回 [**CHString**](chstring.md) 物件，該物件為串連的暫時結果。</span><span class="sxs-lookup"><span data-stu-id="ceb23-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="ceb23-116">這個傳回值可以在同一個運算式中合併數個串連。</span><span class="sxs-lookup"><span data-stu-id="ceb23-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb23-117">備註</span><span class="sxs-lookup"><span data-stu-id="ceb23-117">Remarks</span></span>

<span data-ttu-id="ceb23-118">這兩個引數字串的其中一個必須是 [**CHString**](chstring.md) 物件;另一個可以是字元指標或字元。</span><span class="sxs-lookup"><span data-stu-id="ceb23-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="ceb23-119">請注意，當您使用串連運算子時，可能會發生記憶體例外狀況，因為可以配置新的儲存體來保存暫存資料。</span><span class="sxs-lookup"><span data-stu-id="ceb23-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="ceb23-120">範例</span><span class="sxs-lookup"><span data-stu-id="ceb23-120">Examples</span></span>

<span data-ttu-id="ceb23-121">下列程式碼範例示範如何使用 **CHString：： operator +**：</span><span class="sxs-lookup"><span data-stu-id="ceb23-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="ceb23-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ceb23-122">Requirements</span></span>



| <span data-ttu-id="ceb23-123">需求</span><span class="sxs-lookup"><span data-stu-id="ceb23-123">Requirement</span></span> | <span data-ttu-id="ceb23-124">值</span><span class="sxs-lookup"><span data-stu-id="ceb23-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb23-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ceb23-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb23-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceb23-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ceb23-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ceb23-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb23-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceb23-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ceb23-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ceb23-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceb23-130"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="ceb23-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ceb23-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="ceb23-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="ceb23-132"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ceb23-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="ceb23-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ceb23-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceb23-134"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceb23-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb23-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ceb23-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb23-136">**CHString**</span><span class="sxs-lookup"><span data-stu-id="ceb23-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

