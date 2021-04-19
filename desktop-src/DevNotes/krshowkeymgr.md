---
description: 將 [金鑰管理員] 對話方塊顯示在使用者介面中。
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983960"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="57108-103">KRShowKeyMgr 函式</span><span class="sxs-lookup"><span data-stu-id="57108-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="57108-104">\[這個函式只會包含在 Windows XP 中。</span><span class="sxs-lookup"><span data-stu-id="57108-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="57108-105">它目前不包含在其他任何版本的 Windows 中，也不會包含在任何未來版本的 Windows 中。\]</span><span class="sxs-lookup"><span data-stu-id="57108-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="57108-106">將 [金鑰管理員] 對話方塊顯示在使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="57108-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="57108-107">語法</span><span class="sxs-lookup"><span data-stu-id="57108-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="57108-108">參數</span><span class="sxs-lookup"><span data-stu-id="57108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57108-109">*hwParent*</span><span class="sxs-lookup"><span data-stu-id="57108-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="57108-110">對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="57108-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="57108-111">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57108-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57108-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="57108-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="57108-113">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57108-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57108-114">*pszCmdLine*</span><span class="sxs-lookup"><span data-stu-id="57108-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="57108-115">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57108-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57108-116">*CmdShow*</span><span class="sxs-lookup"><span data-stu-id="57108-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="57108-117">不使用此參數，應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57108-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57108-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="57108-118">Return value</span></span>

<span data-ttu-id="57108-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="57108-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57108-120">備註</span><span class="sxs-lookup"><span data-stu-id="57108-120">Remarks</span></span>

<span data-ttu-id="57108-121">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="57108-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="57108-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="57108-122">Requirements</span></span>



| <span data-ttu-id="57108-123">需求</span><span class="sxs-lookup"><span data-stu-id="57108-123">Requirement</span></span> | <span data-ttu-id="57108-124">值</span><span class="sxs-lookup"><span data-stu-id="57108-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57108-125">DLL</span><span class="sxs-lookup"><span data-stu-id="57108-125">DLL</span></span><br/> | <dl> <span data-ttu-id="57108-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57108-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 
