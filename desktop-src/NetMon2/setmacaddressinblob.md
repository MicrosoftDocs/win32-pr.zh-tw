---
description: SetMacAddressInBlob 函式會設定 BLOB 的要求 MAC 位址。
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: 'SetMacAddressInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850583"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="1c282-103">SetMacAddressInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="1c282-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="1c282-104">**SetMacAddressInBlob** 函式會設定 BLOB 的要求 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="1c282-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c282-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c282-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="1c282-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c282-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c282-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c282-108">要設定之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c282-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="1c282-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c282-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c282-110">要設定之 BLOB **擁有** 者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1c282-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1c282-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c282-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c282-112">要設定之 BLOB **類別目錄** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1c282-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1c282-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c282-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c282-114">要設定之 BLOB **標記** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1c282-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1c282-115">*pMacAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c282-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c282-116">要設定之 BLOB 的 MAC 位址指標。</span><span class="sxs-lookup"><span data-stu-id="1c282-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c282-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c282-117">Return value</span></span>

<span data-ttu-id="1c282-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1c282-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1c282-119">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="1c282-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c282-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c282-120">Requirements</span></span>



| <span data-ttu-id="1c282-121">需求</span><span class="sxs-lookup"><span data-stu-id="1c282-121">Requirement</span></span> | <span data-ttu-id="1c282-122">值</span><span class="sxs-lookup"><span data-stu-id="1c282-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c282-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c282-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1c282-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c282-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1c282-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c282-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1c282-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c282-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c282-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1c282-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c282-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1c282-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1c282-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c282-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c282-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c282-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1c282-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1c282-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c282-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c282-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c282-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c282-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c282-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-137">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="1c282-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="1c282-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




