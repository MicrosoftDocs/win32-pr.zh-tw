---
description: 傳回位於 BLOB 內指定位置的字串。
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: 'GetStringFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468748"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="a5332-103">GetStringFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="a5332-103">GetStringFromBlob function</span></span>

<span data-ttu-id="a5332-104">**GetStringFromBlob** 函式會傳回位於 BLOB 內指定位置的字串。</span><span class="sxs-lookup"><span data-stu-id="a5332-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5332-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5332-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="a5332-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5332-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5332-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5332-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5332-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a5332-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5332-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5332-110">字串所在的 BLOB **擁有** 者區段。</span><span class="sxs-lookup"><span data-stu-id="a5332-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="a5332-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5332-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5332-112">字串所在的 BLOB **類別目錄** 區段。</span><span class="sxs-lookup"><span data-stu-id="a5332-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="a5332-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5332-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5332-114">要求之字串的 **標記** 。</span><span class="sxs-lookup"><span data-stu-id="a5332-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="a5332-115">*ppString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a5332-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5332-116">指向傳回字串之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="a5332-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5332-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5332-117">Return value</span></span>

<span data-ttu-id="a5332-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="a5332-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a5332-119">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="a5332-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="a5332-120">如果指定的 **擁有** 者、 **類別** 或 **標記** 資料不存在，則函式 **會傳回 NMERR \_ BLOB 專案不 \_ \_ \_ \_ 存在**。</span><span class="sxs-lookup"><span data-stu-id="a5332-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5332-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5332-121">Requirements</span></span>



| <span data-ttu-id="a5332-122">需求</span><span class="sxs-lookup"><span data-stu-id="a5332-122">Requirement</span></span> | <span data-ttu-id="a5332-123">值</span><span class="sxs-lookup"><span data-stu-id="a5332-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5332-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5332-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5332-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5332-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a5332-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5332-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5332-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5332-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5332-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a5332-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5332-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a5332-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a5332-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5332-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5332-131"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5332-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5332-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a5332-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5332-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5332-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5332-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5332-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5332-135">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-136">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-137">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-138">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-139">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-140">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-141">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-142">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-143">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="a5332-144">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="a5332-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




