---
description: SetNetworkInfoInBlob 函式會填入 BLOB 中的 NETWORKINFO 結構。
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: 'SetNetworkInfoInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979918"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="4c5cf-103">SetNetworkInfoInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="4c5cf-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="4c5cf-104">**SetNetworkInfoInBlob** 函式會填入 BLOB 中的 **NETWORKINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="4c5cf-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c5cf-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4c5cf-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c5cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c5cf-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c5cf-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5cf-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4c5cf-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="4c5cf-109">*lpNetworkInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c5cf-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5cf-110">函式所填滿之使用者配置 [NETWORKINFO](networkinfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4c5cf-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c5cf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c5cf-111">Return value</span></span>

<span data-ttu-id="4c5cf-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="4c5cf-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4c5cf-113">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="4c5cf-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5cf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c5cf-114">Requirements</span></span>



| <span data-ttu-id="4c5cf-115">需求</span><span class="sxs-lookup"><span data-stu-id="4c5cf-115">Requirement</span></span> | <span data-ttu-id="4c5cf-116">值</span><span class="sxs-lookup"><span data-stu-id="4c5cf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5cf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c5cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5cf-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c5cf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4c5cf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c5cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5cf-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c5cf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c5cf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4c5cf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c5cf-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4c5cf-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4c5cf-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c5cf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c5cf-124"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c5cf-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c5cf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5cf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c5cf-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5cf-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5cf-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c5cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5cf-128">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-133">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="4c5cf-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="4c5cf-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




