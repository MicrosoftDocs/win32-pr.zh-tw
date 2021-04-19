---
description: + = 串連運算子會將字元加入至這個字串的結尾。 運算子接受其他 CHString 物件、字元指標或單一字元。
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString：： operator + = (ChString .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977362"
---
# <a name="chstringoperator"></a><span data-ttu-id="d4b7b-104">CHString：： operator + =</span><span class="sxs-lookup"><span data-stu-id="d4b7b-104">CHString::operator+=</span></span>

<span data-ttu-id="d4b7b-105">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d4b7b-106">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="d4b7b-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d4b7b-107">+ = 串連運算子會將字元加入至這個字串的結尾。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="d4b7b-108">運算子接受其他 [**CHString**](chstring.md) 物件、字元指標或單一字元。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="d4b7b-109">參數</span><span class="sxs-lookup"><span data-stu-id="d4b7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b7b-110"><span id="string"></span><span id="STRING"></span>*字串*</span><span class="sxs-lookup"><span data-stu-id="d4b7b-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="d4b7b-111">串連至此字串的 [**CHString**](chstring.md) 字串。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="d4b7b-112"><span id="ch"></span><span id="CH"></span>*>ch*</span><span class="sxs-lookup"><span data-stu-id="d4b7b-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="d4b7b-113">要串連至此字串的字元。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="d4b7b-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="d4b7b-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="d4b7b-115">要串連至此字串之以 **Null** 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4b7b-116">備註</span><span class="sxs-lookup"><span data-stu-id="d4b7b-116">Remarks</span></span>

<span data-ttu-id="d4b7b-117">請注意，當您使用此串連運算子時，可能會發生記憶體例外狀況，因為新的儲存空間可能會針對新增至這個 [**CHString**](chstring.md) 物件的字元配置。</span><span class="sxs-lookup"><span data-stu-id="d4b7b-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="d4b7b-118">範例</span><span class="sxs-lookup"><span data-stu-id="d4b7b-118">Examples</span></span>

<span data-ttu-id="d4b7b-119">下列範例示範如何使用 **CHString：： operator + =**：</span><span class="sxs-lookup"><span data-stu-id="d4b7b-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="d4b7b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4b7b-120">Requirements</span></span>



| <span data-ttu-id="d4b7b-121">需求</span><span class="sxs-lookup"><span data-stu-id="d4b7b-121">Requirement</span></span> | <span data-ttu-id="d4b7b-122">值</span><span class="sxs-lookup"><span data-stu-id="d4b7b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b7b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4b7b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b7b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4b7b-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d4b7b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4b7b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b7b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4b7b-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d4b7b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d4b7b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b7b-128"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="d4b7b-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d4b7b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4b7b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4b7b-130"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4b7b-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d4b7b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d4b7b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4b7b-132"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b7b-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b7b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4b7b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b7b-134">**CHString**</span><span class="sxs-lookup"><span data-stu-id="d4b7b-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

