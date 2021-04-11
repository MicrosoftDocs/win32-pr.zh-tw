---
description: CHString 指派 (=) 運算子會以新資料重新初始化現有的 CHString 物件。
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString：： operator = (ChString .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026856"
---
# <a name="chstringoperator"></a><span data-ttu-id="d50aa-103">CHString：： operator =</span><span class="sxs-lookup"><span data-stu-id="d50aa-103">CHString::operator=</span></span>

<span data-ttu-id="d50aa-104">\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="d50aa-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d50aa-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="d50aa-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d50aa-106">[**CHString**](chstring.md)指派 (=) 運算子會以新資料重新初始化現有的 CHString 物件。</span><span class="sxs-lookup"><span data-stu-id="d50aa-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="d50aa-107">參數</span><span class="sxs-lookup"><span data-stu-id="d50aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50aa-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*、 *p*</span><span class="sxs-lookup"><span data-stu-id="d50aa-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="d50aa-109">將 [**CHString**](chstring.md) 字串指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="d50aa-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="d50aa-110"><span id="ch"></span><span id="CH"></span>*>ch*</span><span class="sxs-lookup"><span data-stu-id="d50aa-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="d50aa-111">將字元指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="d50aa-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="d50aa-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*、 *psz*</span><span class="sxs-lookup"><span data-stu-id="d50aa-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="d50aa-113">將以 **Null** 終止的字串指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="d50aa-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d50aa-114">備註</span><span class="sxs-lookup"><span data-stu-id="d50aa-114">Remarks</span></span>

<span data-ttu-id="d50aa-115">如果目的地字串 (也就是，左邊的) 已經夠大，足以儲存新的資料，就不會執行任何新的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="d50aa-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="d50aa-116">不過，每當您使用指派運算子時，都可能會發生記憶體例外狀況，因為通常會配置新的儲存體來保存所產生的 [**CHString**](chstring.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d50aa-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="d50aa-117">範例</span><span class="sxs-lookup"><span data-stu-id="d50aa-117">Examples</span></span>

<span data-ttu-id="d50aa-118">下列程式碼範例示範如何使用 **CHString：： operator =**：</span><span class="sxs-lookup"><span data-stu-id="d50aa-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="d50aa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d50aa-119">Requirements</span></span>



| <span data-ttu-id="d50aa-120">需求</span><span class="sxs-lookup"><span data-stu-id="d50aa-120">Requirement</span></span> | <span data-ttu-id="d50aa-121">值</span><span class="sxs-lookup"><span data-stu-id="d50aa-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50aa-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d50aa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d50aa-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d50aa-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d50aa-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d50aa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d50aa-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d50aa-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d50aa-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d50aa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d50aa-127"><dt>ChString (包含 FwCommon) </dt></span><span class="sxs-lookup"><span data-stu-id="d50aa-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d50aa-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d50aa-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d50aa-129"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d50aa-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d50aa-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d50aa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d50aa-131"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d50aa-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d50aa-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d50aa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50aa-133">**CHString**</span><span class="sxs-lookup"><span data-stu-id="d50aa-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

