---
description: 叫用 IDispatch 介面的 helper 功能。
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000289"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="1021c-103">InvokeIDispatch 函式</span><span class="sxs-lookup"><span data-stu-id="1021c-103">InvokeIDispatch function</span></span>

<span data-ttu-id="1021c-104">叫用 IDispatch 介面的 helper 功能。</span><span class="sxs-lookup"><span data-stu-id="1021c-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="1021c-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="1021c-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1021c-106">語法</span><span class="sxs-lookup"><span data-stu-id="1021c-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="1021c-107">參數</span><span class="sxs-lookup"><span data-stu-id="1021c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1021c-108">*pDispatch*</span><span class="sxs-lookup"><span data-stu-id="1021c-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="1021c-109">IDispatch 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="1021c-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="1021c-110">*dispid*</span><span class="sxs-lookup"><span data-stu-id="1021c-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="1021c-111">要傳入的方法、屬性或引數。</span><span class="sxs-lookup"><span data-stu-id="1021c-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="1021c-112">*pDisp*</span><span class="sxs-lookup"><span data-stu-id="1021c-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="1021c-113">要傳入的參數。</span><span class="sxs-lookup"><span data-stu-id="1021c-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="1021c-114">*pVarResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1021c-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1021c-115">接收已抓取值的結構。</span><span class="sxs-lookup"><span data-stu-id="1021c-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1021c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1021c-116">Return value</span></span>

<span data-ttu-id="1021c-117">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1021c-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="1021c-118">如果失敗，可能的傳回碼包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="1021c-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="1021c-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1021c-119">Return code</span></span>                                                                                  | <span data-ttu-id="1021c-120">Description</span><span class="sxs-lookup"><span data-stu-id="1021c-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1021c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1021c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1021c-122">*PDispatch* 的值無效。</span><span class="sxs-lookup"><span data-stu-id="1021c-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1021c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1021c-123">Requirements</span></span>



| <span data-ttu-id="1021c-124">需求</span><span class="sxs-lookup"><span data-stu-id="1021c-124">Requirement</span></span> | <span data-ttu-id="1021c-125">值</span><span class="sxs-lookup"><span data-stu-id="1021c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1021c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1021c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1021c-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1021c-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1021c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1021c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1021c-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="1021c-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1021c-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="1021c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1021c-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1021c-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




