---
description: 關閉自動子類別化。
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980193"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="308ba-103">Ctl3dUnAutoSubclass 函式</span><span class="sxs-lookup"><span data-stu-id="308ba-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="308ba-104">關閉自動子類別化。</span><span class="sxs-lookup"><span data-stu-id="308ba-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="308ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="308ba-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="308ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="308ba-106">Parameters</span></span>

<span data-ttu-id="308ba-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="308ba-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="308ba-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="308ba-108">Return value</span></span>

<span data-ttu-id="308ba-109">如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="308ba-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="308ba-110">備註</span><span class="sxs-lookup"><span data-stu-id="308ba-110">Remarks</span></span>

<span data-ttu-id="308ba-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="308ba-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="308ba-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="308ba-112">Requirements</span></span>



| <span data-ttu-id="308ba-113">需求</span><span class="sxs-lookup"><span data-stu-id="308ba-113">Requirement</span></span> | <span data-ttu-id="308ba-114">值</span><span class="sxs-lookup"><span data-stu-id="308ba-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="308ba-115">DLL</span><span class="sxs-lookup"><span data-stu-id="308ba-115">DLL</span></span><br/> | <dl> <span data-ttu-id="308ba-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="308ba-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
