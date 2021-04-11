---
description: 叫用指定的非同步動作完成時所呼叫的方法。
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: AsyncActionCompletedHandler：： Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113132"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="c0f98-103">AsyncActionCompletedHandler：： Invoke 方法</span><span class="sxs-lookup"><span data-stu-id="c0f98-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="c0f98-104">叫用指定的非同步動作完成時所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="c0f98-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f98-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0f98-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c0f98-106">參數</span><span class="sxs-lookup"><span data-stu-id="c0f98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f98-107">*system.runtime.interopservices.windowsruntime.asyncinfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0f98-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f98-108">類型： \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="c0f98-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="c0f98-109">報告完成的非同步動作。</span><span class="sxs-lookup"><span data-stu-id="c0f98-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f98-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0f98-110">Return value</span></span>

<span data-ttu-id="c0f98-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c0f98-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c0f98-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c0f98-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0f98-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0f98-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f98-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0f98-114">Requirements</span></span>



| <span data-ttu-id="c0f98-115">需求</span><span class="sxs-lookup"><span data-stu-id="c0f98-115">Requirement</span></span> | <span data-ttu-id="c0f98-116">值</span><span class="sxs-lookup"><span data-stu-id="c0f98-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f98-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0f98-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f98-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c0f98-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="c0f98-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0f98-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f98-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0f98-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="c0f98-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c0f98-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f98-122"><dt>Windows .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0f98-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f98-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0f98-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f98-124">**AsyncActionCompletedHandler**</span><span class="sxs-lookup"><span data-stu-id="c0f98-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

