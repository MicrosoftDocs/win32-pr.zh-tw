---
description: 取得物件之 agile 參考的介面識別碼。
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: IAgileReference：： Resolve 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001669"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="a3e61-103">IAgileReference：： Resolve 方法</span><span class="sxs-lookup"><span data-stu-id="a3e61-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="a3e61-104">取得物件之 agile 參考的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3e61-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e61-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3e61-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="a3e61-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3e61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e61-107">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e61-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e61-108">要從 agile 參考中取出的介面介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3e61-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="a3e61-109">它不一定要與註冊的介面相同。</span><span class="sxs-lookup"><span data-stu-id="a3e61-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="a3e61-110">*ppvObjectReference* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a3e61-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e61-111">成功完成時， \* *ppvObjectReference* 是由 *riid* 所指定之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a3e61-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e61-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3e61-112">Return value</span></span>

<span data-ttu-id="a3e61-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a3e61-113">This method can return one of these values.</span></span>



| <span data-ttu-id="a3e61-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3e61-114">Return value</span></span>                                                                              | <span data-ttu-id="a3e61-115">描述</span><span class="sxs-lookup"><span data-stu-id="a3e61-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3e61-116"><dt>S \_ 確定</dt></span><span class="sxs-lookup"><span data-stu-id="a3e61-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="a3e61-117">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="a3e61-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="a3e61-118"><dt>E \_ NOINTERFACE</dt></span><span class="sxs-lookup"><span data-stu-id="a3e61-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="a3e61-119">要求的介面不會在已註冊的物件上執行。</span><span class="sxs-lookup"><span data-stu-id="a3e61-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3e61-120">備註</span><span class="sxs-lookup"><span data-stu-id="a3e61-120">Remarks</span></span>

<span data-ttu-id="a3e61-121">呼叫 [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) 函數，以建立物件的 agile 參考。</span><span class="sxs-lookup"><span data-stu-id="a3e61-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="a3e61-122">呼叫 **resolve** 方法，將物件當地語系化至呼叫 **解析** 的單元中。</span><span class="sxs-lookup"><span data-stu-id="a3e61-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e61-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e61-123">Requirements</span></span>



| <span data-ttu-id="a3e61-124">需求</span><span class="sxs-lookup"><span data-stu-id="a3e61-124">Requirement</span></span> | <span data-ttu-id="a3e61-125">值</span><span class="sxs-lookup"><span data-stu-id="a3e61-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a3e61-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3e61-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e61-127">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e61-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="a3e61-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3e61-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e61-129">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e61-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3e61-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3e61-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e61-131">**IAgileReference**</span><span class="sxs-lookup"><span data-stu-id="a3e61-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="a3e61-132">**RoGetAgileReference**</span><span class="sxs-lookup"><span data-stu-id="a3e61-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




