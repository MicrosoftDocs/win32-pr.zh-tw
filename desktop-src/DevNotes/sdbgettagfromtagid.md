---
description: 抓取與指定 TAGID 相關聯的標記。
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110649"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="86a11-103">SdbGetTagFromTagID 函式</span><span class="sxs-lookup"><span data-stu-id="86a11-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="86a11-104">抓取與指定 **TAGID** 相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="86a11-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a11-105">語法</span><span class="sxs-lookup"><span data-stu-id="86a11-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="86a11-106">參數</span><span class="sxs-lookup"><span data-stu-id="86a11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a11-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86a11-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a11-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="86a11-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="86a11-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86a11-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a11-110">標記的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="86a11-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a11-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="86a11-111">Return value</span></span>

<span data-ttu-id="86a11-112">函數會傳回標記。</span><span class="sxs-lookup"><span data-stu-id="86a11-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a11-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="86a11-113">Requirements</span></span>



| <span data-ttu-id="86a11-114">需求</span><span class="sxs-lookup"><span data-stu-id="86a11-114">Requirement</span></span> | <span data-ttu-id="86a11-115">值</span><span class="sxs-lookup"><span data-stu-id="86a11-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a11-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86a11-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86a11-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86a11-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="86a11-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86a11-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86a11-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86a11-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="86a11-120">DLL</span><span class="sxs-lookup"><span data-stu-id="86a11-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86a11-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a11-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86a11-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86a11-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a11-123">**標記**</span><span class="sxs-lookup"><span data-stu-id="86a11-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="86a11-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="86a11-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




