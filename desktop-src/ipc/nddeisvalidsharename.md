---
description: 判斷共用名稱是否使用適當的語法。
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: 'NDdeIsValidShareName 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973807"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="2f8d9-103">NDdeIsValidShareName 函式</span><span class="sxs-lookup"><span data-stu-id="2f8d9-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="2f8d9-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="2f8d9-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="2f8d9-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="2f8d9-106">判斷共用名稱是否使用適當的語法。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8d9-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f8d9-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="2f8d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f8d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8d9-109">*共用名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f8d9-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8d9-110">要驗證的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-110">The share name to be validated.</span></span> <span data-ttu-id="2f8d9-111">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8d9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f8d9-112">Return value</span></span>

<span data-ttu-id="2f8d9-113">如果共用名稱具有有效的語法，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="2f8d9-114">如果共用名稱的語法無效，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f8d9-115">備註</span><span class="sxs-lookup"><span data-stu-id="2f8d9-115">Remarks</span></span>

<span data-ttu-id="2f8d9-116">[**NDdeShareAdd**](nddeshareadd.md)在建立 DDE 共用時，也會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="2f8d9-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8d9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f8d9-117">Requirements</span></span>



| <span data-ttu-id="2f8d9-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f8d9-118">Requirement</span></span> | <span data-ttu-id="2f8d9-119">值</span><span class="sxs-lookup"><span data-stu-id="2f8d9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8d9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f8d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8d9-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f8d9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f8d9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f8d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8d9-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f8d9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2f8d9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2f8d9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f8d9-125"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f8d9-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f8d9-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f8d9-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f8d9-127"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f8d9-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f8d9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2f8d9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f8d9-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f8d9-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f8d9-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="2f8d9-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2f8d9-131">**NDdeIsValidShareNameW** (Unicode) 和 **NDdeIsValidShareNameA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2f8d9-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="2f8d9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f8d9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8d9-133">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="2f8d9-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="2f8d9-134">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="2f8d9-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="2f8d9-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="2f8d9-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




