---
Description: 抓取指定之 TAGID 的 DWORD 值。
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105929"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="d6123-103">SdbReadDWORDTag 函式</span><span class="sxs-lookup"><span data-stu-id="d6123-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="d6123-104">抓取指定之 **TAGID** 的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="d6123-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6123-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6123-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="d6123-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6123-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6123-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6123-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6123-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="d6123-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6123-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6123-110">對應至要抓取之資料的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="d6123-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="d6123-111">*dwDefault* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6123-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6123-112">失敗時要傳回的預設值。</span><span class="sxs-lookup"><span data-stu-id="d6123-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6123-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6123-113">Return value</span></span>

<span data-ttu-id="d6123-114">函數會在失敗時傳回成功或 *dwDefault* 的值。</span><span class="sxs-lookup"><span data-stu-id="d6123-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6123-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6123-115">Requirements</span></span>



| <span data-ttu-id="d6123-116">需求</span><span class="sxs-lookup"><span data-stu-id="d6123-116">Requirement</span></span> | <span data-ttu-id="d6123-117">值</span><span class="sxs-lookup"><span data-stu-id="d6123-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6123-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6123-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6123-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6123-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d6123-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6123-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6123-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6123-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d6123-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d6123-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6123-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6123-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6123-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6123-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6123-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="d6123-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="d6123-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="d6123-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="d6123-127">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="d6123-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="d6123-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="d6123-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




