---
description: GetProperty 函數會傳回指定之屬性的控制碼。
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: 'GetProperty 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936619"
---
# <a name="getproperty-function"></a><span data-ttu-id="e2b7b-103">GetProperty 函式</span><span class="sxs-lookup"><span data-stu-id="e2b7b-103">GetProperty function</span></span>

<span data-ttu-id="e2b7b-104">**GetProperty** 函數會傳回指定之屬性的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b7b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2b7b-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="e2b7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2b7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b7b-107">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2b7b-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b7b-108">通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="e2b7b-109">*PropertyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2b7b-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b7b-110">屬性的名稱 (例如，總和 **檢查** 碼) 。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b7b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2b7b-111">Return value</span></span>

<span data-ttu-id="e2b7b-112">如果函式成功，則傳回值為屬性的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="e2b7b-113">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b7b-114">備註</span><span class="sxs-lookup"><span data-stu-id="e2b7b-114">Remarks</span></span>

<span data-ttu-id="e2b7b-115">**GetProperty** 函式可以用來取得尋找屬性實例所需的屬性控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="e2b7b-116">用來找出屬性實例的函式是 [FindPropertyInstance](findpropertyinstance.md) (會找出第一個) 的實例，以及找出下一個) 的 [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="e2b7b-117">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetProperty** 函數。</span><span class="sxs-lookup"><span data-stu-id="e2b7b-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b7b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2b7b-118">Requirements</span></span>



| <span data-ttu-id="e2b7b-119">需求</span><span class="sxs-lookup"><span data-stu-id="e2b7b-119">Requirement</span></span> | <span data-ttu-id="e2b7b-120">值</span><span class="sxs-lookup"><span data-stu-id="e2b7b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b7b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2b7b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b7b-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2b7b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e2b7b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2b7b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b7b-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2b7b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e2b7b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e2b7b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b7b-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e2b7b-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e2b7b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2b7b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2b7b-128"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2b7b-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e2b7b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e2b7b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2b7b-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2b7b-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b7b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2b7b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b7b-132">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="e2b7b-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="e2b7b-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="e2b7b-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




