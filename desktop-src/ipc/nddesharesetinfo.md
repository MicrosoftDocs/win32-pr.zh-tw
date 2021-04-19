---
description: 設定 DDE 共用資訊。 這通常是在編輯之後完成。
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: 'NDdeShareSetInfo 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973806"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="0e42e-104">NDdeShareSetInfo 函式</span><span class="sxs-lookup"><span data-stu-id="0e42e-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="0e42e-105">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="0e42e-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="0e42e-106">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="0e42e-107">設定 DDE 共用資訊。</span><span class="sxs-lookup"><span data-stu-id="0e42e-107">Sets DDE share information.</span></span> <span data-ttu-id="0e42e-108">這通常是在編輯之後完成。</span><span class="sxs-lookup"><span data-stu-id="0e42e-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e42e-109">語法</span><span class="sxs-lookup"><span data-stu-id="0e42e-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="0e42e-110">參數</span><span class="sxs-lookup"><span data-stu-id="0e42e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e42e-111">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e42e-112">要修改其 DSDM 的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0e42e-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="0e42e-113">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e42e-114">要修改其資訊的共用名稱名稱。</span><span class="sxs-lookup"><span data-stu-id="0e42e-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="0e42e-115">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0e42e-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e42e-116">*nLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e42e-117">資訊層級。</span><span class="sxs-lookup"><span data-stu-id="0e42e-117">The information level.</span></span> <span data-ttu-id="0e42e-118">此參數必須是2。</span><span class="sxs-lookup"><span data-stu-id="0e42e-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="0e42e-119">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e42e-120">[**NDDESHAREINFO**](nddeshareinfo-str.md)結構的指標，指定要儲存在 DSDM 中的 DDE 共用資訊。</span><span class="sxs-lookup"><span data-stu-id="0e42e-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="0e42e-121">目前會修改整個 DDE 共用資訊，也就是說，不會進行部分編輯。</span><span class="sxs-lookup"><span data-stu-id="0e42e-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="0e42e-122">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0e42e-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e42e-123">*cBufSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e42e-124">*LpBuffer* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0e42e-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0e42e-125">*sParmNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e42e-126">要修改的參數索引。</span><span class="sxs-lookup"><span data-stu-id="0e42e-126">The parameter index to be modified.</span></span> <span data-ttu-id="0e42e-127">目前的執行不支援部分修改;因此，此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e42e-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e42e-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e42e-128">Return value</span></span>

<span data-ttu-id="0e42e-129">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="0e42e-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="0e42e-130">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="0e42e-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e42e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e42e-131">Requirements</span></span>



| <span data-ttu-id="0e42e-132">需求</span><span class="sxs-lookup"><span data-stu-id="0e42e-132">Requirement</span></span> | <span data-ttu-id="0e42e-133">值</span><span class="sxs-lookup"><span data-stu-id="0e42e-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e42e-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e42e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0e42e-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0e42e-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e42e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0e42e-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e42e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0e42e-138">標頭</span><span class="sxs-lookup"><span data-stu-id="0e42e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e42e-139"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e42e-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e42e-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e42e-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e42e-141"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e42e-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e42e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0e42e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e42e-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e42e-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e42e-144">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="0e42e-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e42e-145">**NDdeShareSetInfoW** (Unicode) 和 **NDdeShareSetInfoA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="0e42e-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0e42e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e42e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e42e-147">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="0e42e-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="0e42e-148">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="0e42e-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="0e42e-149">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="0e42e-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="0e42e-150">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0e42e-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




