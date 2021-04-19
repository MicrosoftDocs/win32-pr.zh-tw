---
description: 抓取指定之 TAGID 的二進位資料。
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: SdbGetBinaryTagData 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972125"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="fb961-103">SdbGetBinaryTagData 函式</span><span class="sxs-lookup"><span data-stu-id="fb961-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="fb961-104">抓取指定之 **TAGID** 的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="fb961-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb961-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb961-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="fb961-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb961-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb961-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb961-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fb961-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="fb961-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb961-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb961-110">對應至要抓取之資料的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="fb961-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb961-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb961-111">Return value</span></span>

<span data-ttu-id="fb961-112">函數會傳回二進位資料的指標，如果 **TAGID** 無效，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="fb961-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb961-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb961-113">Requirements</span></span>



| <span data-ttu-id="fb961-114">需求</span><span class="sxs-lookup"><span data-stu-id="fb961-114">Requirement</span></span> | <span data-ttu-id="fb961-115">值</span><span class="sxs-lookup"><span data-stu-id="fb961-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb961-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb961-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fb961-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb961-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fb961-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb961-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fb961-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb961-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fb961-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fb961-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb961-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb961-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb961-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb961-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb961-123">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="fb961-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="fb961-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="fb961-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="fb961-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="fb961-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="fb961-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="fb961-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




