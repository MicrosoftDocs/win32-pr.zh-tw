---
description: 將應用程式取消註冊為 CTL3D 的用戶端。
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001928"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="cf89b-103">Ctl3dUnregister 函式</span><span class="sxs-lookup"><span data-stu-id="cf89b-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="cf89b-104">將應用程式取消註冊為 CTL3D 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="cf89b-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf89b-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf89b-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="cf89b-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf89b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf89b-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="cf89b-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="cf89b-108">要以用戶端的形式取消註冊之應用程式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cf89b-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf89b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf89b-109">Return value</span></span>

<span data-ttu-id="cf89b-110">如果將應用程式取消註冊為 CTL3D 的用戶端，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cf89b-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf89b-111">備註</span><span class="sxs-lookup"><span data-stu-id="cf89b-111">Remarks</span></span>

<span data-ttu-id="cf89b-112">使用 CTL3D 的應用程式應該在 WinMain 中呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="cf89b-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="cf89b-113">不在 VGA 解析度的系統上無法使用3D 效果。</span><span class="sxs-lookup"><span data-stu-id="cf89b-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="cf89b-114">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="cf89b-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf89b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf89b-115">Requirements</span></span>



| <span data-ttu-id="cf89b-116">需求</span><span class="sxs-lookup"><span data-stu-id="cf89b-116">Requirement</span></span> | <span data-ttu-id="cf89b-117">值</span><span class="sxs-lookup"><span data-stu-id="cf89b-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf89b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cf89b-118">DLL</span></span><br/> | <dl> <span data-ttu-id="cf89b-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf89b-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
