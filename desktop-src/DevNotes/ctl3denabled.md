---
description: 驗證控制項是否可以使用3D 效果。
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981321"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="7faee-103">Ctl3dEnabled 函式</span><span class="sxs-lookup"><span data-stu-id="7faee-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="7faee-104">驗證控制項是否可以使用3D 效果。</span><span class="sxs-lookup"><span data-stu-id="7faee-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faee-105">語法</span><span class="sxs-lookup"><span data-stu-id="7faee-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="7faee-106">參數</span><span class="sxs-lookup"><span data-stu-id="7faee-106">Parameters</span></span>

<span data-ttu-id="7faee-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="7faee-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7faee-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7faee-108">Return value</span></span>

<span data-ttu-id="7faee-109">如果控制項可以使用3D 效果，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7faee-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7faee-110">備註</span><span class="sxs-lookup"><span data-stu-id="7faee-110">Remarks</span></span>

<span data-ttu-id="7faee-111">在 Windows 4.0 或更新版本中， **Ctl3dEnabled** 和 [**Ctl3dRegister**](ctl3dregister.md) 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7faee-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="7faee-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="7faee-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7faee-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7faee-113">Requirements</span></span>



| <span data-ttu-id="7faee-114">需求</span><span class="sxs-lookup"><span data-stu-id="7faee-114">Requirement</span></span> | <span data-ttu-id="7faee-115">值</span><span class="sxs-lookup"><span data-stu-id="7faee-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7faee-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7faee-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7faee-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7faee-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
