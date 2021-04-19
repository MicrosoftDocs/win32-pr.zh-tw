---
description: 將應用程式註冊為 CTL3D 的用戶端。
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990966"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="c9a6d-103">Ctl3dRegister 函式</span><span class="sxs-lookup"><span data-stu-id="c9a6d-103">Ctl3dRegister function</span></span>

<span data-ttu-id="c9a6d-104">將應用程式註冊為 CTL3D 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="c9a6d-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a6d-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9a6d-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="c9a6d-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a6d-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="c9a6d-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a6d-108">要註冊為用戶端之應用程式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c9a6d-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a6d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9a6d-109">Return value</span></span>

<span data-ttu-id="c9a6d-110">如果3D 效果為使用中，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c9a6d-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a6d-111">備註</span><span class="sxs-lookup"><span data-stu-id="c9a6d-111">Remarks</span></span>

<span data-ttu-id="c9a6d-112">使用 CTL3D 的應用程式應該在 WinMain 中呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="c9a6d-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="c9a6d-113">不在 VGA 解析度的系統上無法使用3D 效果。</span><span class="sxs-lookup"><span data-stu-id="c9a6d-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="c9a6d-114">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c9a6d-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a6d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9a6d-115">Requirements</span></span>



| <span data-ttu-id="c9a6d-116">需求</span><span class="sxs-lookup"><span data-stu-id="c9a6d-116">Requirement</span></span> | <span data-ttu-id="c9a6d-117">值</span><span class="sxs-lookup"><span data-stu-id="c9a6d-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a6d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a6d-118">DLL</span></span><br/> | <dl> <span data-ttu-id="c9a6d-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a6d-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
