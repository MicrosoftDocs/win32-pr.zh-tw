---
description: 在 BLOB 中的指定位置設定字串。
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: 'SetStringInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191486"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="ff448-103">SetStringInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="ff448-103">SetStringInBlob function</span></span>

<span data-ttu-id="ff448-104">**SetStringInBlob** 函式會在 BLOB 中的指定位置設定字串。</span><span class="sxs-lookup"><span data-stu-id="ff448-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff448-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff448-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="ff448-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff448-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff448-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff448-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff448-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ff448-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="ff448-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff448-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff448-110">BLOB 的 **擁有** 者區段的指標，其中會設定字串。</span><span class="sxs-lookup"><span data-stu-id="ff448-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="ff448-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff448-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff448-112">BLOB **類別目錄** 區段的指標，其中會設定字串。</span><span class="sxs-lookup"><span data-stu-id="ff448-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="ff448-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff448-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff448-114">要求之字串的 **標記** 指標。</span><span class="sxs-lookup"><span data-stu-id="ff448-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="ff448-115">*pString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff448-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff448-116">指標，指向將傳回字串指標的變數。</span><span class="sxs-lookup"><span data-stu-id="ff448-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff448-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff448-117">Return value</span></span>

<span data-ttu-id="ff448-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="ff448-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ff448-119">如果函式不成功，則傳回值會是指出問題的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="ff448-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="ff448-120">如果指定的 **擁有** 者、 **類別** 或 **標記** 資訊不存在，則傳回值為 NMERR \_ BLOB 專案不 \_ \_ \_ \_ 存在。</span><span class="sxs-lookup"><span data-stu-id="ff448-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff448-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff448-121">Requirements</span></span>



| <span data-ttu-id="ff448-122">需求</span><span class="sxs-lookup"><span data-stu-id="ff448-122">Requirement</span></span> | <span data-ttu-id="ff448-123">值</span><span class="sxs-lookup"><span data-stu-id="ff448-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff448-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff448-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ff448-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff448-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ff448-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff448-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ff448-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff448-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff448-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ff448-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff448-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ff448-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff448-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff448-131"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff448-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ff448-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff448-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff448-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff448-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff448-135">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-136">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-137">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-138">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-139">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-140">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-141">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-142">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="ff448-143">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="ff448-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 




