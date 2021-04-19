---
title: STOWED_EXCEPTION_INFORMATION_V2 結構
description: 包含 stowed 例外狀況資訊。
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 結構 Windows 錯誤報告
- PSTOWED_EXCEPTION_INFORMATION_V2 結構指標 Windows 錯誤報告
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966531"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="e9193-105">STOWED \_ 例外狀況 \_ 資訊 \_ V2 結構</span><span class="sxs-lookup"><span data-stu-id="e9193-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="e9193-106">包含 stowed 例外狀況資訊。</span><span class="sxs-lookup"><span data-stu-id="e9193-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9193-107">語法</span><span class="sxs-lookup"><span data-stu-id="e9193-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="e9193-108">成員</span><span class="sxs-lookup"><span data-stu-id="e9193-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9193-109">**標頭**</span><span class="sxs-lookup"><span data-stu-id="e9193-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-110">類型： **[ **STOWED \_ 例外狀況 \_ 資訊 \_ 標頭**](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="e9193-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-111">[**STOWED \_ 例外狀況 \_ 資訊 \_ 標頭**](stowed-exception-information-header.md)結構，包含此父結構的資訊。</span><span class="sxs-lookup"><span data-stu-id="e9193-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9193-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="e9193-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-113">類型： **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-114">Stowed 例外狀況的 [**HRESULT**](/windows/desktop/WinProg/windows-data-types) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e9193-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="e9193-115">**ExceptionForm**</span><span class="sxs-lookup"><span data-stu-id="e9193-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-116">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-117">識別例外狀況形式的2位值。</span><span class="sxs-lookup"><span data-stu-id="e9193-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="e9193-118">值</span><span class="sxs-lookup"><span data-stu-id="e9193-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="e9193-119">意義</span><span class="sxs-lookup"><span data-stu-id="e9193-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="e9193-120"><dt>**STOWED \_例外狀況 \_ 表單 \_ 二進位**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e9193-121">此值表示例外狀況的格式為二進位。</span><span class="sxs-lookup"><span data-stu-id="e9193-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="e9193-122"><dt>**STOWED \_例外狀況 \_ 表單 \_ 文字**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="e9193-123">這個值表示例外狀況的格式是文字。</span><span class="sxs-lookup"><span data-stu-id="e9193-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e9193-124">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="e9193-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-125">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-126">表示引發例外狀況之執行緒的30位值。</span><span class="sxs-lookup"><span data-stu-id="e9193-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="e9193-127">值會在儲存時右移至2個位。</span><span class="sxs-lookup"><span data-stu-id="e9193-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="e9193-128">若要將它轉換回有效的執行緒識別碼，請將值向左移位2。</span><span class="sxs-lookup"><span data-stu-id="e9193-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="e9193-129">例如：</span><span class="sxs-lookup"><span data-stu-id="e9193-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="e9193-130"> (*未命名的結構*) </span><span class="sxs-lookup"><span data-stu-id="e9193-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="e9193-131">只有當 **ExceptionForm** 成員設定為 **STOWED \_ 例外狀況 \_ 表單 \_ 二進位** 時，此嵌套結構的成員才有效。</span><span class="sxs-lookup"><span data-stu-id="e9193-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="e9193-132">**ExceptionAddress**</span><span class="sxs-lookup"><span data-stu-id="e9193-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-133">類型： **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-134">包含例外狀況位址的指標。</span><span class="sxs-lookup"><span data-stu-id="e9193-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="e9193-135">**StackTraceWordSize**</span><span class="sxs-lookup"><span data-stu-id="e9193-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-136">類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-137">**StackTrace** 成員指向之堆疊追蹤中每個單字的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e9193-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="e9193-138">若為32位平臺，此值會設為4，64位平臺則設為8。</span><span class="sxs-lookup"><span data-stu-id="e9193-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="e9193-139">**StackTraceWords**</span><span class="sxs-lookup"><span data-stu-id="e9193-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-140">類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-141">**StackTrace** 成員指向之堆疊追蹤中的文字數目。</span><span class="sxs-lookup"><span data-stu-id="e9193-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="e9193-142">單字數目等於陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="e9193-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="e9193-143">**StackTrace**</span><span class="sxs-lookup"><span data-stu-id="e9193-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-144">類型： **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-145">包含堆疊追蹤之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="e9193-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e9193-146"> (*未命名的結構*) </span><span class="sxs-lookup"><span data-stu-id="e9193-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="e9193-147">只有當 **ExceptionForm** 成員設定為 **STOWED \_ 例外狀況 \_ 表單 \_ 文字** 時，此嵌套結構的成員才有效。</span><span class="sxs-lookup"><span data-stu-id="e9193-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="e9193-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="e9193-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-149">類型： **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-150">以 null 結束的字串指標，其中包含例外狀況的錯誤文字。</span><span class="sxs-lookup"><span data-stu-id="e9193-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e9193-151">**NestedExceptionType**</span><span class="sxs-lookup"><span data-stu-id="e9193-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-152">類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-153">指定 **NestedException** 成員指向之物件類型的32位值。</span><span class="sxs-lookup"><span data-stu-id="e9193-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="e9193-154">使用此位元組交換類型定義宏來定義值，該宏假設為位元組由小到小：</span><span class="sxs-lookup"><span data-stu-id="e9193-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="e9193-155">以下是一些常見的類型定義：</span><span class="sxs-lookup"><span data-stu-id="e9193-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="e9193-156">值</span><span class="sxs-lookup"><span data-stu-id="e9193-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="e9193-157">意義</span><span class="sxs-lookup"><span data-stu-id="e9193-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="e9193-158"><dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ NONE**</dt> <dt> (0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="e9193-159">此值指定沒有任何嵌套的例外狀況物件。</span><span class="sxs-lookup"><span data-stu-id="e9193-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="e9193-160"><dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ WIN32**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' W32E ' )</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="e9193-161">這個值會指定 **NestedException** 成員指向 [**例外狀況 \_ 記錄**](/windows/desktop/api/winnt/ns-winnt-exception_record) 物件。</span><span class="sxs-lookup"><span data-stu-id="e9193-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="e9193-162"><dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ STOWED**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' STOW ' )</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="e9193-163">這個值會指定 **NestedException** 成員指向另一個 stowed 例外狀況物件。</span><span class="sxs-lookup"><span data-stu-id="e9193-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="e9193-164">其他 stowed 例外狀況物件可以是 **stowed \_ 例外狀況 \_ 資訊 \_ V2** 物件或具有有效 **標頭** 成員的不同版本，也就是包含有效 [**Stowed 例外狀況 \_ \_ 資訊 \_ 標**](stowed-exception-information-header.md)頭的 **標頭** 成員。</span><span class="sxs-lookup"><span data-stu-id="e9193-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="e9193-165"><dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ CLR**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' CLR1 ' )</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="e9193-166">這個值會指定 **NestedException** 成員指向 ' CLR1 ' 例外狀況物件。</span><span class="sxs-lookup"><span data-stu-id="e9193-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="e9193-167"><dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ LEO**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' LEO1 ' )</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="e9193-168">這個值會指定 **NestedException** 成員指向語言例外狀況物件。</span><span class="sxs-lookup"><span data-stu-id="e9193-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="e9193-169">**NestedException**</span><span class="sxs-lookup"><span data-stu-id="e9193-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="e9193-170">類型： **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9193-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9193-171">嵌套例外狀況類型的指標。</span><span class="sxs-lookup"><span data-stu-id="e9193-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="e9193-172">物件的類型是由 **NestedExceptionType** 成員所表示。</span><span class="sxs-lookup"><span data-stu-id="e9193-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9193-173">備註</span><span class="sxs-lookup"><span data-stu-id="e9193-173">Remarks</span></span>

<span data-ttu-id="e9193-174">**STOWED \_例外狀況 \_ 資訊 \_ V2** 和 [**STOWED 例外狀況 \_ \_ 資訊 \_ 標頭**](stowed-exception-information-header.md) 目前未定義于可公開取得的標頭中，因此您必須先在原始程式碼中定義它們，然後才能使用它們。</span><span class="sxs-lookup"><span data-stu-id="e9193-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="e9193-175">**STOWED \_ 例外狀況 \_ 資訊 \_ V1** 結構與此結構相同，但不包含 **NestedExceptionType** 和 **NestedException** 成員。</span><span class="sxs-lookup"><span data-stu-id="e9193-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9193-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9193-176">Requirements</span></span>



| <span data-ttu-id="e9193-177">需求</span><span class="sxs-lookup"><span data-stu-id="e9193-177">Requirement</span></span> | <span data-ttu-id="e9193-178">值</span><span class="sxs-lookup"><span data-stu-id="e9193-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e9193-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9193-179">Minimum supported client</span></span><br/> | <span data-ttu-id="e9193-180">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9193-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9193-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9193-181">Minimum supported server</span></span><br/> | <span data-ttu-id="e9193-182">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9193-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e9193-183">標頭</span><span class="sxs-lookup"><span data-stu-id="e9193-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9193-184"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="e9193-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9193-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9193-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9193-186">**例外狀況 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="e9193-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="e9193-187">**STOWED \_ 例外狀況 \_ 資訊 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="e9193-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

