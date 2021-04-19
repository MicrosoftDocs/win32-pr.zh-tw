---
description: GetNetworkInfoFromBlob 函式會從指定的 BLOB 抓取網路資訊。
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: 'GetNetworkInfoFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988077"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="a361f-103">GetNetworkInfoFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="a361f-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="a361f-104">**GetNetworkInfoFromBlob** 函式會從指定的 BLOB 抓取網路資訊。</span><span class="sxs-lookup"><span data-stu-id="a361f-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="a361f-105">語法</span><span class="sxs-lookup"><span data-stu-id="a361f-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a361f-106">參數</span><span class="sxs-lookup"><span data-stu-id="a361f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a361f-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a361f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a361f-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a361f-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a361f-109">*lpNetworkInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a361f-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a361f-110">填入的使用者配置 [NETWORKINFO](networkinfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a361f-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a361f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a361f-111">Return value</span></span>

<span data-ttu-id="a361f-112">如果 **GetNetworkInfoFromBlob** 函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="a361f-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a361f-113">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="a361f-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a361f-114">備註</span><span class="sxs-lookup"><span data-stu-id="a361f-114">Remarks</span></span>

<span data-ttu-id="a361f-115">網路資訊會儲存在 [BLOB NPP **擁有** 者] 類別的 [blob **NetworkInfo** ] 區段中。</span><span class="sxs-lookup"><span data-stu-id="a361f-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="a361f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a361f-116">Requirements</span></span>



| <span data-ttu-id="a361f-117">需求</span><span class="sxs-lookup"><span data-stu-id="a361f-117">Requirement</span></span> | <span data-ttu-id="a361f-118">值</span><span class="sxs-lookup"><span data-stu-id="a361f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a361f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a361f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a361f-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a361f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a361f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a361f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a361f-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a361f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a361f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a361f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a361f-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a361f-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a361f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a361f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a361f-126"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a361f-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a361f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a361f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a361f-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a361f-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a361f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a361f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a361f-130">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-131">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-132">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-133">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-135">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-136">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-137">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-138">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="a361f-139">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="a361f-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




