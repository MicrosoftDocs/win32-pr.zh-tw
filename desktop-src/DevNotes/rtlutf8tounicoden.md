---
description: 使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的來源字串轉譯成 Unicode 字串。
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: 'RtlUTF8ToUnicodeN 函式 (Wdm) '
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187668"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="03afb-103">RtlUTF8ToUnicodeN 函式</span><span class="sxs-lookup"><span data-stu-id="03afb-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="03afb-104">使用8位 Unicode 轉換格式 (UTF-8) 字碼頁，將指定的來源字串轉譯成 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="03afb-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="03afb-105">語法</span><span class="sxs-lookup"><span data-stu-id="03afb-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="03afb-106">參數</span><span class="sxs-lookup"><span data-stu-id="03afb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03afb-107">*UnicodeStringDestination* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="03afb-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03afb-108">呼叫端配置的緩衝區的指標，此緩衝區會接收翻譯的字串。</span><span class="sxs-lookup"><span data-stu-id="03afb-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="03afb-109">*UnicodeStringMaxByteCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03afb-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03afb-110">要在 *UnicodeStringDestination* 寫入的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="03afb-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="03afb-111">如果這個值導致轉譯的字串被截斷， **RtlUTF8ToUnicodeN** 會傳回錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="03afb-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="03afb-112">*UnicodeStringActualByteCount* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="03afb-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03afb-113">呼叫端組態變數的指標，此變數會接收翻譯字串的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="03afb-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="03afb-114">這個參數是選擇性的，而且可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03afb-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="03afb-115">如果字串被截斷，傳回的數位就會計算實際截斷的字串計數。</span><span class="sxs-lookup"><span data-stu-id="03afb-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="03afb-116">*UTF8StringSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03afb-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03afb-117">要轉譯之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="03afb-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="03afb-118">*UTF8StringByteCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03afb-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03afb-119">*UTF8StringSource* 中字串的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="03afb-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03afb-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="03afb-120">Return value</span></span>

<span data-ttu-id="03afb-121">**RtlUTF8ToUnicodeN** 會傳回下列其中一個 NTSTATUS 值：</span><span class="sxs-lookup"><span data-stu-id="03afb-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="03afb-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="03afb-122">Return code</span></span>                                                                                                  | <span data-ttu-id="03afb-123">Description</span><span class="sxs-lookup"><span data-stu-id="03afb-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03afb-124"><dt>**狀態 \_ 成功**</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="03afb-125">字串已轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="03afb-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="03afb-126"><dt>**狀態 \_ 部分 \_ 未 \_ 對應**</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="03afb-127">遇到不正確輸入字元，並被取代。</span><span class="sxs-lookup"><span data-stu-id="03afb-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="03afb-128">此狀態會被視為成功狀態。</span><span class="sxs-lookup"><span data-stu-id="03afb-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="03afb-129"><dt>**狀態 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="03afb-130">*UnicodeStringDestination* 和 *UnicodeStringActualByteCount* 的兩個指標都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03afb-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="03afb-131"><dt>**狀態 \_ 不正確 \_ 參數 \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="03afb-132">*UTF8StringSource* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03afb-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="03afb-133"><dt>**狀態 \_ 緩衝區 \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="03afb-134">*UnicodeStringDestination* 已被截斷。</span><span class="sxs-lookup"><span data-stu-id="03afb-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="03afb-135">備註</span><span class="sxs-lookup"><span data-stu-id="03afb-135">Remarks</span></span>

<span data-ttu-id="03afb-136">雖然 *UnicodeStringActualByteCount* 是選擇性的，而且可以是 **Null**，但呼叫端應該提供它的儲存空間，因為接收的長度可以用來判斷轉換是否成功。</span><span class="sxs-lookup"><span data-stu-id="03afb-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="03afb-137">如果輸出已截斷並遇到不正確輸入字元，則函式會傳回狀態 \_ 緩衝區 \_ 太 \_ 小的錯誤。</span><span class="sxs-lookup"><span data-stu-id="03afb-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="03afb-138">如果 *UnicodeStringDestination* 設定為 **Null** ，則函式會傳回所需的位元組數目來裝載轉譯的字串，而不會在 *UnicodeStringActualByteCount* 中進行任何截斷。</span><span class="sxs-lookup"><span data-stu-id="03afb-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="03afb-139">除非 *UnicodeStringDestination* 和 *UTF8StringSource* 指標相等，否則 **RtlUTF8ToUnicodeN** 不會修改來源字串。</span><span class="sxs-lookup"><span data-stu-id="03afb-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="03afb-140">傳回的 Unicode 字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="03afb-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="03afb-141">**RtlUTF8ToUnicodeN** 的呼叫端必須以 IRQL < 分派 \_ 層級執行。</span><span class="sxs-lookup"><span data-stu-id="03afb-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="03afb-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="03afb-142">Requirements</span></span>



| <span data-ttu-id="03afb-143">需求</span><span class="sxs-lookup"><span data-stu-id="03afb-143">Requirement</span></span> | <span data-ttu-id="03afb-144">值</span><span class="sxs-lookup"><span data-stu-id="03afb-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="03afb-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03afb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="03afb-146">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03afb-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03afb-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03afb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="03afb-148">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03afb-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="03afb-149">標頭</span><span class="sxs-lookup"><span data-stu-id="03afb-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="03afb-150"><dt>Wdm</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="03afb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="03afb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03afb-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03afb-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03afb-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03afb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03afb-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="03afb-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




