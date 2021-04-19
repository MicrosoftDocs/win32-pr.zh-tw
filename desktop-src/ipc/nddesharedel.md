---
description: 從 DDE 共用資料庫管理員刪除 DDE 共用 (DSDM) 。
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: 'NDdeShareDel 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967078"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="3df6a-103">NDdeShareDel 函式</span><span class="sxs-lookup"><span data-stu-id="3df6a-103">NDdeShareDel function</span></span>

<span data-ttu-id="3df6a-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="3df6a-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="3df6a-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="3df6a-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="3df6a-106">從 DDE 共用資料庫管理員刪除 DDE 共用 (DSDM) 。</span><span class="sxs-lookup"><span data-stu-id="3df6a-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="3df6a-107">語法</span><span class="sxs-lookup"><span data-stu-id="3df6a-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="3df6a-108">參數</span><span class="sxs-lookup"><span data-stu-id="3df6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df6a-109">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3df6a-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df6a-110">要修改其 DSDM 的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3df6a-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="3df6a-111">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3df6a-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df6a-112">要從 DSDM 中刪除的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="3df6a-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="3df6a-113">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3df6a-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3df6a-114">*wReserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3df6a-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df6a-115">保留的。</span><span class="sxs-lookup"><span data-stu-id="3df6a-115">Reserved.</span></span> <span data-ttu-id="3df6a-116">此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="3df6a-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df6a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3df6a-117">Return value</span></span>

<span data-ttu-id="3df6a-118">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="3df6a-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="3df6a-119">如果函式失敗，則傳回值是可透過呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)轉譯成文字錯誤訊息的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3df6a-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3df6a-120">備註</span><span class="sxs-lookup"><span data-stu-id="3df6a-120">Remarks</span></span>

<span data-ttu-id="3df6a-121">若要從 DSDM 中刪除 DDE 共用，您必須具有適當的許可權。</span><span class="sxs-lookup"><span data-stu-id="3df6a-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="3df6a-122">共用建立者具有刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="3df6a-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df6a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3df6a-123">Requirements</span></span>



| <span data-ttu-id="3df6a-124">需求</span><span class="sxs-lookup"><span data-stu-id="3df6a-124">Requirement</span></span> | <span data-ttu-id="3df6a-125">值</span><span class="sxs-lookup"><span data-stu-id="3df6a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3df6a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3df6a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3df6a-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3df6a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3df6a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3df6a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3df6a-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3df6a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3df6a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3df6a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df6a-131"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3df6a-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="3df6a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="3df6a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="3df6a-133"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3df6a-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3df6a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3df6a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df6a-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df6a-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="3df6a-136">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="3df6a-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3df6a-137">**NDdeShareDelW** (Unicode) 和 **NDdeShareDelA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="3df6a-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="3df6a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3df6a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df6a-139">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="3df6a-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="3df6a-140">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="3df6a-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




