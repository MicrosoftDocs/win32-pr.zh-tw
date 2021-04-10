---
description: 使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的 Unicode 字串轉譯成新的字元字串。
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: 'RtlUnicodeToUTF8N 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110433"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="4e62f-103">RtlUnicodeToUTF8N 函式</span><span class="sxs-lookup"><span data-stu-id="4e62f-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="4e62f-104">使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的 Unicode 字串轉譯成新的字元字串。</span><span class="sxs-lookup"><span data-stu-id="4e62f-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e62f-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e62f-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="4e62f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e62f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e62f-107">*UTF8StringDestination* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e62f-108">呼叫端配置的緩衝區指標，用來接收翻譯的字串。</span><span class="sxs-lookup"><span data-stu-id="4e62f-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="4e62f-109">*UTF8StringMaxByteCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e62f-110">要寫入至 *UTF8StringDestination* 的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4e62f-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="4e62f-111">如果這個值導致轉譯的字串被截斷， **RtlUnicodeToUTF8N** 會傳回錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="4e62f-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="4e62f-112">*UTF8StringActualByteCount* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4e62f-113">呼叫端組態變數的指標，此變數會接收翻譯字串的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4e62f-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="4e62f-114">這個參數是選擇性的，而且可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e62f-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="4e62f-115">如果字串被截斷，傳回的數位就會計算實際截斷的字串計數。</span><span class="sxs-lookup"><span data-stu-id="4e62f-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="4e62f-116">*UnicodeStringSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e62f-117">要轉譯的 Unicode 來源字串指標。</span><span class="sxs-lookup"><span data-stu-id="4e62f-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="4e62f-118">\* UnicodeStringByteCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e62f-119">指定 *UnicodeStringSource* 參數指向的 Unicode 來源字串中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4e62f-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e62f-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e62f-120">Return value</span></span>

<span data-ttu-id="4e62f-121">**RtlUnicodeToUTF8N** 會傳回下列其中一個 NTSTATUS 值：</span><span class="sxs-lookup"><span data-stu-id="4e62f-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="4e62f-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4e62f-122">Return code</span></span>                                                                                                  | <span data-ttu-id="4e62f-123">Description</span><span class="sxs-lookup"><span data-stu-id="4e62f-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e62f-124"><dt>**狀態 \_ 成功**</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="4e62f-125">Unicode 字串已轉換為 UTF-8。</span><span class="sxs-lookup"><span data-stu-id="4e62f-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="4e62f-126"><dt>**狀態 \_ 部分 \_ 未 \_ 對應**</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="4e62f-127">遇到不正確輸入字元，並被取代。</span><span class="sxs-lookup"><span data-stu-id="4e62f-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="4e62f-128">此狀態會被視為成功狀態。</span><span class="sxs-lookup"><span data-stu-id="4e62f-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="4e62f-129"><dt>**狀態 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="4e62f-130">*UTF8StringDestination* 和 *UTF8StringActualByteCount* 的兩個指標都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e62f-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="4e62f-131"><dt>**狀態 \_ 不正確 \_ 參數 \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="4e62f-132">*UnicodeStringSource* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e62f-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="4e62f-133"><dt>**狀態 \_ 緩衝區 \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="4e62f-134">*UTF8StringDestination* 已被截斷。</span><span class="sxs-lookup"><span data-stu-id="4e62f-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="4e62f-135">備註</span><span class="sxs-lookup"><span data-stu-id="4e62f-135">Remarks</span></span>

<span data-ttu-id="4e62f-136">雖然 *UTF8StringActualByteCount* 是選擇性的，而且可以是 **Null**，但呼叫端應該提供它的儲存空間，因為接收的長度可以用來判斷轉換是否成功。</span><span class="sxs-lookup"><span data-stu-id="4e62f-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="4e62f-137">此常式不會修改來源字串。</span><span class="sxs-lookup"><span data-stu-id="4e62f-137">This routine does not modify the source string.</span></span> <span data-ttu-id="4e62f-138">如果指定的 *UnicodeStringSource* 包含 null 結束字元，且給定的 *UTF8StringMaxByteCount* 不會造成截斷，則會傳回以 null 終止的 utf-8 字串。</span><span class="sxs-lookup"><span data-stu-id="4e62f-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="4e62f-139">如果輸出已截斷並遇到不正確輸入字元，則函式會傳回狀態 \_ 緩衝區 \_ 太 \_ 小的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e62f-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="4e62f-140">如果 *UTF8StringDestination* 設定為 **Null** ，則函式會傳回所需的位元組數目來裝載轉譯的字串，而不會在 *UTF8StringActualByteCount* 中進行任何截斷。</span><span class="sxs-lookup"><span data-stu-id="4e62f-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="4e62f-141">**RtlUnicodeToUTF8N** 的呼叫端必須以 IRQL < 分派 \_ 層級執行。</span><span class="sxs-lookup"><span data-stu-id="4e62f-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e62f-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e62f-142">Requirements</span></span>



| <span data-ttu-id="4e62f-143">需求</span><span class="sxs-lookup"><span data-stu-id="4e62f-143">Requirement</span></span> | <span data-ttu-id="4e62f-144">值</span><span class="sxs-lookup"><span data-stu-id="4e62f-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e62f-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e62f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4e62f-146">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4e62f-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e62f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4e62f-148">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e62f-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4e62f-149">標頭</span><span class="sxs-lookup"><span data-stu-id="4e62f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e62f-150"><dt>Wdm</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="4e62f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="4e62f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e62f-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e62f-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e62f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e62f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e62f-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="4e62f-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 




