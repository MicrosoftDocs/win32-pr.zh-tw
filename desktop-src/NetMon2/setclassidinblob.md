---
description: SetClassIDInBlob 函式會設定 BLOB 的命名類別識別碼值。
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: 'SetClassIDInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979085"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="51ab2-103">SetClassIDInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="51ab2-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="51ab2-104">**SetClassIDInBlob** 函式會設定 BLOB 的命名類別識別碼值。</span><span class="sxs-lookup"><span data-stu-id="51ab2-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ab2-105">語法</span><span class="sxs-lookup"><span data-stu-id="51ab2-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="51ab2-106">參數</span><span class="sxs-lookup"><span data-stu-id="51ab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ab2-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ab2-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="51ab2-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="51ab2-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ab2-110">已設定之 BLOB **擁有** 者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="51ab2-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="51ab2-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ab2-112">已設定之 BLOB **類別目錄** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="51ab2-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="51ab2-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ab2-114">已設定之 BLOB **標記** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="51ab2-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="51ab2-115">*pClsID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ab2-116">已設定之 BLOB 的類別識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="51ab2-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ab2-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="51ab2-117">Return value</span></span>

<span data-ttu-id="51ab2-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="51ab2-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="51ab2-119">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="51ab2-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ab2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="51ab2-120">Requirements</span></span>



| <span data-ttu-id="51ab2-121">需求</span><span class="sxs-lookup"><span data-stu-id="51ab2-121">Requirement</span></span> | <span data-ttu-id="51ab2-122">值</span><span class="sxs-lookup"><span data-stu-id="51ab2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51ab2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51ab2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="51ab2-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="51ab2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51ab2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="51ab2-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51ab2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51ab2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="51ab2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="51ab2-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="51ab2-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="51ab2-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="51ab2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="51ab2-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="51ab2-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="51ab2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="51ab2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51ab2-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51ab2-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ab2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51ab2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ab2-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="51ab2-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="51ab2-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




