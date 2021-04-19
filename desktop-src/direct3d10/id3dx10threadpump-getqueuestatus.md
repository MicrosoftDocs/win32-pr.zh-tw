---
description: 取得執行緒抽取內三個佇列中的專案數。
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'ID3DX10ThreadPump：： GetQueueStatus 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999053"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="90e6f-103">ID3DX10ThreadPump：： GetQueueStatus 方法</span><span class="sxs-lookup"><span data-stu-id="90e6f-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="90e6f-104">取得執行緒抽取內三個佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="90e6f-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e6f-105">語法</span><span class="sxs-lookup"><span data-stu-id="90e6f-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="90e6f-106">參數</span><span class="sxs-lookup"><span data-stu-id="90e6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e6f-107">*pIoQueue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90e6f-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e6f-108">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="90e6f-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90e6f-109">I/o 佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="90e6f-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="90e6f-110">*pProcessQueue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90e6f-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e6f-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="90e6f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90e6f-112">進程佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="90e6f-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="90e6f-113">*pDeviceQueue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90e6f-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e6f-114">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="90e6f-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90e6f-115">裝置佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="90e6f-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90e6f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="90e6f-116">Return value</span></span>

<span data-ttu-id="90e6f-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90e6f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90e6f-118">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="90e6f-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90e6f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="90e6f-119">Requirements</span></span>



| <span data-ttu-id="90e6f-120">需求</span><span class="sxs-lookup"><span data-stu-id="90e6f-120">Requirement</span></span> | <span data-ttu-id="90e6f-121">值</span><span class="sxs-lookup"><span data-stu-id="90e6f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90e6f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="90e6f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="90e6f-123"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="90e6f-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="90e6f-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="90e6f-124">Library</span></span><br/> | <dl> <span data-ttu-id="90e6f-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90e6f-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e6f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90e6f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e6f-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="90e6f-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="90e6f-128">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="90e6f-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
