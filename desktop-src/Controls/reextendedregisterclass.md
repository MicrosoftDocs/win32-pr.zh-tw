---
title: REExtendedRegisterClass 函式
description: 註冊兩個類別名稱（REListBox20W 和 RECombobox20W），可用來建立 Rich Edit listbox 或 combobox 視窗。
ms.assetid: D27A97A8-8B44-4C07-9903-8D958BF97109
keywords:
- REExtendedRegisterClass 函式 Windows 控制項
topic_type:
- apiref
api_name:
- REExtendedRegisterClass
api_location:
- Riched20.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 965394eaf71812e503c31aa2c65e0128a75dbfe3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994076"
---
# <a name="reextendedregisterclass-function"></a><span data-ttu-id="de683-104">REExtendedRegisterClass 函式</span><span class="sxs-lookup"><span data-stu-id="de683-104">REExtendedRegisterClass function</span></span>

<span data-ttu-id="de683-105">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="de683-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="de683-106">未來的版本可能不支援此功能。\]</span><span class="sxs-lookup"><span data-stu-id="de683-106">This function may not be supported in future versions.\]</span></span>

<span data-ttu-id="de683-107">註冊兩個類別名稱（REListBox20W 和 RECombobox20W），可用來建立 Rich Edit listbox 或 combobox 視窗。</span><span class="sxs-lookup"><span data-stu-id="de683-107">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="de683-108">語法</span><span class="sxs-lookup"><span data-stu-id="de683-108">Syntax</span></span>


```C++
BOOL WINAPI REExtendedRegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="de683-109">參數</span><span class="sxs-lookup"><span data-stu-id="de683-109">Parameters</span></span>

<span data-ttu-id="de683-110">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="de683-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de683-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="de683-111">Return value</span></span>

<span data-ttu-id="de683-112">如果成功，則傳回 TRUE，否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="de683-112">Returns TRUE if successful, or FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de683-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="de683-113">Requirements</span></span>



| <span data-ttu-id="de683-114">需求</span><span class="sxs-lookup"><span data-stu-id="de683-114">Requirement</span></span> | <span data-ttu-id="de683-115">值</span><span class="sxs-lookup"><span data-stu-id="de683-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de683-116">標頭</span><span class="sxs-lookup"><span data-stu-id="de683-116">Header</span></span><br/> | <dl> <span data-ttu-id="de683-117"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="de683-117"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="de683-118">DLL</span><span class="sxs-lookup"><span data-stu-id="de683-118">DLL</span></span><br/>    | <dl> <span data-ttu-id="de683-119"><dt>Riched20.dll (Rich Edit 3.0 版) </dt></span><span class="sxs-lookup"><span data-stu-id="de683-119"><dt>Riched20.dll (Rich Edit version 3.0)</dt></span></span> </dl> |



 

 





