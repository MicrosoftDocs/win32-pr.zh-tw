---
description: FindPropertyInstance 函數會尋找 hProperty 參數所指定之屬性的第一個實例。
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: 'FindPropertyInstance 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973221"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="3ca06-103">FindPropertyInstance 函式</span><span class="sxs-lookup"><span data-stu-id="3ca06-103">FindPropertyInstance function</span></span>

<span data-ttu-id="3ca06-104">**FindPropertyInstance** 函數會尋找 *hProperty* 參數所指定之屬性的第一個實例。</span><span class="sxs-lookup"><span data-stu-id="3ca06-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca06-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ca06-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="3ca06-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ca06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca06-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ca06-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca06-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ca06-108">Handle to the frame.</span></span> <span data-ttu-id="3ca06-109">[GetFrame](getframe.md)函式的呼叫可以取出框架控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ca06-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3ca06-110">*hProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ca06-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca06-111">您要尋找的屬性的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ca06-111">Handle to the property you want to find.</span></span> <span data-ttu-id="3ca06-112">[GetProperty](getproperty.md)函式的呼叫可以取出屬性控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ca06-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca06-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ca06-113">Return value</span></span>

<span data-ttu-id="3ca06-114">如果函式成功 (也就是，如果) 找到此屬性，則傳回值為屬性之第一個實例的指標。</span><span class="sxs-lookup"><span data-stu-id="3ca06-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="3ca06-115">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3ca06-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca06-116">備註</span><span class="sxs-lookup"><span data-stu-id="3ca06-116">Remarks</span></span>

<span data-ttu-id="3ca06-117">若要取出屬性的下一個實例，請呼叫 [FindPropertyInstanceRestart](findpropertyinstancerestart.md)。</span><span class="sxs-lookup"><span data-stu-id="3ca06-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="3ca06-118">[*專家*](e.md) 和 [*剖析*](p.md)器可以呼叫 **FindPropertyInstance** 函數。</span><span class="sxs-lookup"><span data-stu-id="3ca06-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca06-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ca06-119">Requirements</span></span>



| <span data-ttu-id="3ca06-120">需求</span><span class="sxs-lookup"><span data-stu-id="3ca06-120">Requirement</span></span> | <span data-ttu-id="3ca06-121">值</span><span class="sxs-lookup"><span data-stu-id="3ca06-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca06-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ca06-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca06-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca06-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3ca06-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ca06-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca06-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca06-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3ca06-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3ca06-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca06-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3ca06-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3ca06-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ca06-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ca06-129"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ca06-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ca06-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca06-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ca06-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ca06-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca06-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ca06-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca06-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="3ca06-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




