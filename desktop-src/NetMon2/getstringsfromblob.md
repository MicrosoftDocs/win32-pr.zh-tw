---
description: 使用連續呼叫來取得指定範圍內的所有字串。
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: 'GetStringsFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936615"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="fb867-103">GetStringsFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="fb867-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="fb867-104">**GetStringsFromBlob** 函式會使用連續呼叫來取得指定範圍內的所有字串。</span><span class="sxs-lookup"><span data-stu-id="fb867-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb867-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb867-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="fb867-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb867-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb867-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb867-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fb867-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-109">*pRequestedOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb867-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-110">要從中取得字串的擁有者區段指標。</span><span class="sxs-lookup"><span data-stu-id="fb867-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-111">*pRequestedCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb867-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-112">要從中取得字串的類別目錄區段指標。</span><span class="sxs-lookup"><span data-stu-id="fb867-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-113">*pRequestedTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb867-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-114">要求之字串的標記指標。</span><span class="sxs-lookup"><span data-stu-id="fb867-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-115">*ppReturnedOwnerName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb867-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-116">指向將傳回 **擁有** 者名稱之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="fb867-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-117">*ppReturnedCategoryName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb867-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-118">指向將傳回 **分類** 名稱之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="fb867-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-119">*ppReturnedTagName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb867-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-120">指向變數的指標，指向將傳回 **標記** 名稱的位置。</span><span class="sxs-lookup"><span data-stu-id="fb867-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-121">*ppReturnedString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb867-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-122">指向將傳回字串名稱之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="fb867-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="fb867-123">*pRestartKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb867-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb867-124">變數的指標，其中將會指定並傳回重新啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb867-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb867-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb867-125">Return value</span></span>

<span data-ttu-id="fb867-126">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="fb867-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fb867-127">如果函式不成功，則傳回值會是指出問題的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="fb867-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="fb867-128">如果 **擁有** 者、 **類別** 和 **標記** 資訊的指定組合不存在，則傳回值為 **NMERR \_ BLOB 專案不 \_ \_ \_ \_ 存在**。</span><span class="sxs-lookup"><span data-stu-id="fb867-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="fb867-129">當 BLOB 完全在一開始指定的界限內進行時，此函 **式 \_ 會傳回 NMERR BLOB 專案不 \_ \_ \_ \_ 存在**，而且 *pRestartKey* 參數會指向零。</span><span class="sxs-lookup"><span data-stu-id="fb867-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb867-130">備註</span><span class="sxs-lookup"><span data-stu-id="fb867-130">Remarks</span></span>

<span data-ttu-id="fb867-131">在 **GetStringsFromBlob** 函數的初始呼叫上， *pRestartKey* 參數會指向包含零值的變數。</span><span class="sxs-lookup"><span data-stu-id="fb867-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="fb867-132">只有當重新啟動金鑰為零時，才能使用 *pRequested* 參數。</span><span class="sxs-lookup"><span data-stu-id="fb867-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="fb867-133">在後續的呼叫中，當 *pRestartKey* 有非零值時，會忽略 *pRequested* 參數。</span><span class="sxs-lookup"><span data-stu-id="fb867-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="fb867-134">在初始呼叫上，所有專案都可能指向 **Null**，這會設定查詢來傳回 BLOB 中的每個專案，每個後續呼叫一個專案。</span><span class="sxs-lookup"><span data-stu-id="fb867-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="fb867-135">指定擁有者會將傳回的字串限制為只有該擁有者。</span><span class="sxs-lookup"><span data-stu-id="fb867-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="fb867-136">類別和標籤也有類似的限制，另外請注意，如果指定了類別，也必須指定擁有者，如果指定了標籤，則類別 (，因此必須指定擁有者) 。</span><span class="sxs-lookup"><span data-stu-id="fb867-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="fb867-137">當初次呼叫 **GetStringsFromBlob** 時， *pRestartKey* 會指向新的值，此值應在下一次呼叫函式時指定以取得下一個值。</span><span class="sxs-lookup"><span data-stu-id="fb867-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb867-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb867-138">Requirements</span></span>



| <span data-ttu-id="fb867-139">需求</span><span class="sxs-lookup"><span data-stu-id="fb867-139">Requirement</span></span> | <span data-ttu-id="fb867-140">值</span><span class="sxs-lookup"><span data-stu-id="fb867-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb867-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb867-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fb867-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb867-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fb867-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb867-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fb867-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb867-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb867-145">標頭</span><span class="sxs-lookup"><span data-stu-id="fb867-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb867-146"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fb867-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="fb867-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb867-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb867-148"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb867-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb867-149">DLL</span><span class="sxs-lookup"><span data-stu-id="fb867-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb867-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb867-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb867-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb867-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb867-152">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-153">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-154">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-155">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-156">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-157">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-158">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-159">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-160">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="fb867-161">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="fb867-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 




