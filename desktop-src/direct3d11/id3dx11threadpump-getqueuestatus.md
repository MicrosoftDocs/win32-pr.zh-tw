---
title: 'ID3DX11ThreadPump GetQueueStatus 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 取得執行緒抽取內三個佇列中的專案數。
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- GetQueueStatus 方法 Direct3D 11
- GetQueueStatus 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，GetQueueStatus 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974532"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="f71c7-107">ID3DX11ThreadPump：： GetQueueStatus 方法</span><span class="sxs-lookup"><span data-stu-id="f71c7-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="f71c7-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f71c7-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f71c7-109">取得執行緒抽取內三個佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f71c7-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71c7-110">語法</span><span class="sxs-lookup"><span data-stu-id="f71c7-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="f71c7-111">參數</span><span class="sxs-lookup"><span data-stu-id="f71c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71c7-112">*pIoQueue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f71c7-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71c7-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f71c7-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f71c7-114">I/o 佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f71c7-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="f71c7-115">*pProcessQueue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f71c7-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71c7-116">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f71c7-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f71c7-117">進程佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f71c7-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="f71c7-118">*pDeviceQueue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f71c7-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71c7-119">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f71c7-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f71c7-120">裝置佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f71c7-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71c7-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="f71c7-121">Return value</span></span>

<span data-ttu-id="f71c7-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f71c7-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f71c7-123">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f71c7-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f71c7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f71c7-124">Requirements</span></span>



| <span data-ttu-id="f71c7-125">需求</span><span class="sxs-lookup"><span data-stu-id="f71c7-125">Requirement</span></span> | <span data-ttu-id="f71c7-126">值</span><span class="sxs-lookup"><span data-stu-id="f71c7-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71c7-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f71c7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f71c7-128"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="f71c7-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="f71c7-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="f71c7-129">Library</span></span><br/> | <dl> <span data-ttu-id="f71c7-130"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f71c7-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f71c7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f71c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71c7-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="f71c7-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="f71c7-133">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f71c7-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

