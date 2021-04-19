---
description: 關閉指定控制項的子類別化。
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994841"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="1f72e-103">Ctl3dUnsubclassCtl 函式</span><span class="sxs-lookup"><span data-stu-id="1f72e-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="1f72e-104">關閉指定控制項的子類別化。</span><span class="sxs-lookup"><span data-stu-id="1f72e-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f72e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f72e-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="1f72e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f72e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f72e-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="1f72e-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1f72e-108">控制項視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f72e-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f72e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f72e-109">Return value</span></span>

<span data-ttu-id="1f72e-110">如果成功將控制項子類別化，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1f72e-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f72e-111">備註</span><span class="sxs-lookup"><span data-stu-id="1f72e-111">Remarks</span></span>

<span data-ttu-id="1f72e-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="1f72e-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f72e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f72e-113">Requirements</span></span>



| <span data-ttu-id="1f72e-114">需求</span><span class="sxs-lookup"><span data-stu-id="1f72e-114">Requirement</span></span> | <span data-ttu-id="1f72e-115">值</span><span class="sxs-lookup"><span data-stu-id="1f72e-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f72e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1f72e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1f72e-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f72e-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f72e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f72e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f72e-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="1f72e-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
