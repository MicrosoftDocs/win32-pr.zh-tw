---
Description: 抓取指定之 TAGID 的字串。
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: SdbReadStringTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934997"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="cdf08-103">SdbReadStringTag 函式</span><span class="sxs-lookup"><span data-stu-id="cdf08-103">SdbReadStringTag function</span></span>

<span data-ttu-id="cdf08-104">抓取指定之 **TAGID** 的字串。</span><span class="sxs-lookup"><span data-stu-id="cdf08-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf08-105">語法</span><span class="sxs-lookup"><span data-stu-id="cdf08-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="cdf08-106">參數</span><span class="sxs-lookup"><span data-stu-id="cdf08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf08-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf08-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf08-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cdf08-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="cdf08-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf08-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf08-110">對應至要抓取之資料的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="cdf08-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cdf08-111">*pwszBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cdf08-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf08-112">接收字串的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cdf08-112">The buffer that receives the string.</span></span> <span data-ttu-id="cdf08-113">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cdf08-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cdf08-114">*cchBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf08-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf08-115">*PwszBuffer* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cdf08-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf08-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdf08-116">Return value</span></span>

<span data-ttu-id="cdf08-117">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="cdf08-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf08-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdf08-118">Requirements</span></span>



| <span data-ttu-id="cdf08-119">需求</span><span class="sxs-lookup"><span data-stu-id="cdf08-119">Requirement</span></span> | <span data-ttu-id="cdf08-120">值</span><span class="sxs-lookup"><span data-stu-id="cdf08-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf08-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdf08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf08-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdf08-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cdf08-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdf08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf08-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdf08-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cdf08-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf08-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf08-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdf08-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdf08-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdf08-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf08-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="cdf08-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="cdf08-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="cdf08-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="cdf08-130">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="cdf08-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="cdf08-131">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="cdf08-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




