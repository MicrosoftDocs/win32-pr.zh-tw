---
description: 抓取指定之 TAGID 的字串資料。
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: SdbGetStringTagPtr 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936271"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="8fc56-103">SdbGetStringTagPtr 函式</span><span class="sxs-lookup"><span data-stu-id="8fc56-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="8fc56-104">抓取指定之 **TAGID** 的字串資料。</span><span class="sxs-lookup"><span data-stu-id="8fc56-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc56-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fc56-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="8fc56-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fc56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc56-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fc56-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc56-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8fc56-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="8fc56-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fc56-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc56-110">對應至要抓取之字串資料的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="8fc56-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc56-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fc56-111">Return value</span></span>

<span data-ttu-id="8fc56-112">函數會傳回字串資料的指標，如果 **TAGID** 無效或不是類型 **標記 \_ 類型 \_ 字串** 或 **標記 \_ 類型 \_ STRINGREF**，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8fc56-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc56-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fc56-113">Requirements</span></span>



| <span data-ttu-id="8fc56-114">需求</span><span class="sxs-lookup"><span data-stu-id="8fc56-114">Requirement</span></span> | <span data-ttu-id="8fc56-115">值</span><span class="sxs-lookup"><span data-stu-id="8fc56-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc56-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fc56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc56-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fc56-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8fc56-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fc56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc56-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fc56-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8fc56-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc56-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc56-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc56-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc56-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fc56-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc56-123">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="8fc56-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="8fc56-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="8fc56-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="8fc56-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="8fc56-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="8fc56-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="8fc56-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




