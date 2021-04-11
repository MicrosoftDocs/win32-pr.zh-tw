---
description: 取得非同步動作的結果。
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: IAsyncAction：： GetResults 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191351"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="ab5e0-103">IAsyncAction：： GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="ab5e0-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="ab5e0-104">取得非同步動作的結果。</span><span class="sxs-lookup"><span data-stu-id="ab5e0-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab5e0-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="ab5e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab5e0-106">Parameters</span></span>

<span data-ttu-id="ab5e0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ab5e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab5e0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab5e0-108">Return value</span></span>

<span data-ttu-id="ab5e0-109">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab5e0-109">Type: **HRESULT**</span></span>

<span data-ttu-id="ab5e0-110">這個方法一律會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ab5e0-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab5e0-111">備註</span><span class="sxs-lookup"><span data-stu-id="ab5e0-111">Remarks</span></span>

<span data-ttu-id="ab5e0-112">如果目前的實有動態類型的 [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)，則呼叫 **GetResults** 方法不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="ab5e0-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5e0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab5e0-113">Requirements</span></span>



| <span data-ttu-id="ab5e0-114">需求</span><span class="sxs-lookup"><span data-stu-id="ab5e0-114">Requirement</span></span> | <span data-ttu-id="ab5e0-115">值</span><span class="sxs-lookup"><span data-stu-id="ab5e0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5e0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab5e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5e0-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ab5e0-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="ab5e0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab5e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5e0-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab5e0-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="ab5e0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ab5e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab5e0-121"><dt>Windows .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab5e0-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab5e0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab5e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5e0-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="ab5e0-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
