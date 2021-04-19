---
description: 處理使用 CTL3D 之應用程式的系統色彩變更。
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985770"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="5a200-103">Ctl3dColorChange 函式</span><span class="sxs-lookup"><span data-stu-id="5a200-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="5a200-104">處理使用 CTL3D 之應用程式的系統色彩變更。</span><span class="sxs-lookup"><span data-stu-id="5a200-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a200-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a200-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="5a200-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a200-106">Parameters</span></span>

<span data-ttu-id="5a200-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="5a200-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a200-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a200-108">Return value</span></span>

<span data-ttu-id="5a200-109">如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5a200-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a200-110">備註</span><span class="sxs-lookup"><span data-stu-id="5a200-110">Remarks</span></span>

<span data-ttu-id="5a200-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5a200-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="5a200-112">此函式應針對 **WM \_ SYSCOLORCHANGE** 訊息在應用程式的主要視窗程式中呼叫，如下所示。</span><span class="sxs-lookup"><span data-stu-id="5a200-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="5a200-113">範例</span><span class="sxs-lookup"><span data-stu-id="5a200-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="5a200-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a200-114">Requirements</span></span>



| <span data-ttu-id="5a200-115">需求</span><span class="sxs-lookup"><span data-stu-id="5a200-115">Requirement</span></span> | <span data-ttu-id="5a200-116">值</span><span class="sxs-lookup"><span data-stu-id="5a200-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a200-117">DLL</span><span class="sxs-lookup"><span data-stu-id="5a200-117">DLL</span></span><br/> | <dl> <span data-ttu-id="5a200-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a200-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
