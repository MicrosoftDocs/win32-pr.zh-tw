---
title: 'MB_GetString 函數 (User .h) '
description: 傳回標準訊息方塊按鈕的字串。
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- MB_GetString 函式對話方塊
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999669"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="e0b77-104">MB \_ GetString 函式</span><span class="sxs-lookup"><span data-stu-id="e0b77-104">MB\_GetString function</span></span>

<span data-ttu-id="e0b77-105">傳回標準訊息方塊按鈕的字串。</span><span class="sxs-lookup"><span data-stu-id="e0b77-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b77-106">語法</span><span class="sxs-lookup"><span data-stu-id="e0b77-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="e0b77-107">參數</span><span class="sxs-lookup"><span data-stu-id="e0b77-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b77-108">*wBtn*</span><span class="sxs-lookup"><span data-stu-id="e0b77-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b77-109">要傳回的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0b77-109">The id of the string to return.</span></span> <span data-ttu-id="e0b77-110">這些是由 winuser 中所列的對話方塊命令識別碼值所識別。</span><span class="sxs-lookup"><span data-stu-id="e0b77-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b77-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0b77-111">Return value</span></span>

<span data-ttu-id="e0b77-112">字串，如果找不到則為 Null。</span><span class="sxs-lookup"><span data-stu-id="e0b77-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b77-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0b77-113">Requirements</span></span>



| <span data-ttu-id="e0b77-114">需求</span><span class="sxs-lookup"><span data-stu-id="e0b77-114">Requirement</span></span> | <span data-ttu-id="e0b77-115">值</span><span class="sxs-lookup"><span data-stu-id="e0b77-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b77-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e0b77-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0b77-117"><dt>使用者。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b77-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="e0b77-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e0b77-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0b77-119"><dt>User32</dt></span><span class="sxs-lookup"><span data-stu-id="e0b77-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e0b77-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b77-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0b77-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b77-121"><dt>User32.dll</dt></span></span> </dl> |



 

 





