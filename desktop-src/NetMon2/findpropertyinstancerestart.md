---
description: 尋找 hProperty 參數所指定之屬性的下一個實例。
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: 'FindPropertyInstanceRestart 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998445"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="b8634-103">FindPropertyInstanceRestart 函式</span><span class="sxs-lookup"><span data-stu-id="b8634-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="b8634-104">**FindPropertyInstanceRestart** 函數會尋找 *hProperty* 參數所指定之屬性的下一個實例。</span><span class="sxs-lookup"><span data-stu-id="b8634-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8634-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8634-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="b8634-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8634-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8634-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8634-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8634-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8634-108">A handle to the frame.</span></span> <span data-ttu-id="b8634-109">[GetFrame](getframe.md)函式的呼叫可以取出框架控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8634-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b8634-110">*hProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8634-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8634-111">要尋找之屬性的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8634-111">A handle to the property to find.</span></span> <span data-ttu-id="b8634-112">[GetProperty](getproperty.md)函式的呼叫可以取出屬性控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8634-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b8634-113">*lpRestartKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8634-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8634-114">當做搜尋起點使用的屬性實例指標。</span><span class="sxs-lookup"><span data-stu-id="b8634-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="b8634-115">如果 *lpRestartKey* 參數設定為 **Null**，則會根據 *DirForward* 參數的值，從框架的開頭或框架的結尾開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="b8634-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="b8634-116">如果 *lpRestartKey* 指向 **Null**，則會在 *DirForward* 為 **TRUE** 時從框架的開頭開始搜尋，如果參數為 **FALSE**，則會從框架的結尾開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="b8634-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b8634-117">*DirForward* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8634-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8634-118">搜尋方向的指標。</span><span class="sxs-lookup"><span data-stu-id="b8634-118">An indicator of the search direction.</span></span> <span data-ttu-id="b8634-119">如果值為 **TRUE**，搜尋會從目前的位置移至框架的結尾。</span><span class="sxs-lookup"><span data-stu-id="b8634-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="b8634-120">如果值為 **FALSE**，搜尋會從目前的位置移至框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="b8634-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8634-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8634-121">Return value</span></span>

<span data-ttu-id="b8634-122">如果函式成功，則傳回值是下一個有效的 **LPPROPERTYINST**。</span><span class="sxs-lookup"><span data-stu-id="b8634-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="b8634-123">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8634-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8634-124">備註</span><span class="sxs-lookup"><span data-stu-id="b8634-124">Remarks</span></span>

<span data-ttu-id="b8634-125">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **FindPropertyInstanceRestart** 函數。</span><span class="sxs-lookup"><span data-stu-id="b8634-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8634-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8634-126">Requirements</span></span>



| <span data-ttu-id="b8634-127">需求</span><span class="sxs-lookup"><span data-stu-id="b8634-127">Requirement</span></span> | <span data-ttu-id="b8634-128">值</span><span class="sxs-lookup"><span data-stu-id="b8634-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8634-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8634-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b8634-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8634-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b8634-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8634-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b8634-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8634-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8634-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b8634-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8634-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b8634-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b8634-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8634-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8634-136"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8634-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8634-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b8634-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8634-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8634-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8634-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8634-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8634-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="b8634-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="b8634-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="b8634-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




