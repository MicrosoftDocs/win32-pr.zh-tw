---
description: 抓取與指定進程相關聯之指定物件的物件控制碼。
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: 'ObFindHandleForObject 函式 (Ntosp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847126"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="97570-103">ObFindHandleForObject 函式</span><span class="sxs-lookup"><span data-stu-id="97570-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="97570-104">\[此函式已過時，可能會在未來的 Windows 版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="97570-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="97570-105">請避免使用此函數。\]</span><span class="sxs-lookup"><span data-stu-id="97570-105">Avoid using this function.\]</span></span>

<span data-ttu-id="97570-106">抓取與指定進程相關聯之指定物件的物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="97570-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="97570-107">語法</span><span class="sxs-lookup"><span data-stu-id="97570-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="97570-108">參數</span><span class="sxs-lookup"><span data-stu-id="97570-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97570-109">*進程* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97570-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97570-110">處理序。</span><span class="sxs-lookup"><span data-stu-id="97570-110">The process.</span></span> <span data-ttu-id="97570-111">**IoGetCurrentProcess** 或 **PsGetCurrentProcess** 函數會傳回此控制碼。</span><span class="sxs-lookup"><span data-stu-id="97570-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="97570-112">*物件* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97570-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97570-113">物件的指標。</span><span class="sxs-lookup"><span data-stu-id="97570-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="97570-114">*Reserved1* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="97570-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97570-115">保留的。</span><span class="sxs-lookup"><span data-stu-id="97570-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97570-116">*Reserved2* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="97570-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97570-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="97570-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97570-118">*控制碼* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="97570-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97570-119">物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="97570-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97570-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="97570-120">Return value</span></span>

<span data-ttu-id="97570-121">如果找到相符的函式，則函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="97570-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="97570-122">備註</span><span class="sxs-lookup"><span data-stu-id="97570-122">Remarks</span></span>

<span data-ttu-id="97570-123">此函式可在 Ntoskrnl.exe 中取得，而且只能從核心模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="97570-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="97570-124">對應的匯入程式庫可透過 Windows 驅動程式套件 (WDK) 取得。</span><span class="sxs-lookup"><span data-stu-id="97570-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="97570-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="97570-125">Requirements</span></span>



| <span data-ttu-id="97570-126">需求</span><span class="sxs-lookup"><span data-stu-id="97570-126">Requirement</span></span> | <span data-ttu-id="97570-127">值</span><span class="sxs-lookup"><span data-stu-id="97570-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97570-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97570-128">Minimum supported client</span></span><br/> | <span data-ttu-id="97570-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97570-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="97570-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97570-130">Minimum supported server</span></span><br/> | <span data-ttu-id="97570-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97570-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97570-132">標頭</span><span class="sxs-lookup"><span data-stu-id="97570-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="97570-133"><dt>Ntosp。h</dt></span><span class="sxs-lookup"><span data-stu-id="97570-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="97570-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="97570-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="97570-135"><dt>Ntoskrnl.exe .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97570-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




