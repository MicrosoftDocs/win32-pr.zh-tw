---
description: '\_針對使用 CTL3D 的應用程式處理 WM CTLCOLOR 訊息。'
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996438"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="ec0ba-103">Ctl3dCtlColorEx 函式</span><span class="sxs-lookup"><span data-stu-id="ec0ba-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="ec0ba-104">針對使用 CTL3D 的應用程式處理 **WM \_ CTLCOLOR** 訊息。</span><span class="sxs-lookup"><span data-stu-id="ec0ba-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec0ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec0ba-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="ec0ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec0ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec0ba-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="ec0ba-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="ec0ba-108">應用程式的 **WM \_ CTLCOLOR** 訊息。</span><span class="sxs-lookup"><span data-stu-id="ec0ba-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="ec0ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec0ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec0ba-110"> (DC) 的顯示內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec0ba-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="ec0ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec0ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec0ba-112">子視窗的控制碼 (控制項) 。</span><span class="sxs-lookup"><span data-stu-id="ec0ba-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec0ba-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec0ba-113">Return value</span></span>

<span data-ttu-id="ec0ba-114">如果函式成功，則傳回適當筆刷的控制碼;否則會傳回， `(HBRUSH)(0)` 表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec0ba-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0ba-115">備註</span><span class="sxs-lookup"><span data-stu-id="ec0ba-115">Remarks</span></span>

<span data-ttu-id="ec0ba-116">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ec0ba-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0ba-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec0ba-117">Requirements</span></span>



| <span data-ttu-id="ec0ba-118">需求</span><span class="sxs-lookup"><span data-stu-id="ec0ba-118">Requirement</span></span> | <span data-ttu-id="ec0ba-119">值</span><span class="sxs-lookup"><span data-stu-id="ec0ba-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0ba-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ec0ba-120">DLL</span></span><br/> | <dl> <span data-ttu-id="ec0ba-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec0ba-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
