---
title: 'ID3DX11DataProcessor Process 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 處理資料。
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- 處理方法 Direct3D 11
- 處理方法 Direct3D 11，ID3DX11DataProcessor 介面
- ID3DX11DataProcessor 介面 Direct3D 11，Process 方法
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514625"
---
# <a name="id3dx11dataprocessorprocess-method"></a><span data-ttu-id="fd0c5-107">ID3DX11DataProcessor：:P rocess 方法</span><span class="sxs-lookup"><span data-stu-id="fd0c5-107">ID3DX11DataProcessor::Process method</span></span>

> [!Note]  
> <span data-ttu-id="fd0c5-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="fd0c5-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="fd0c5-109">處理資料。</span><span class="sxs-lookup"><span data-stu-id="fd0c5-109">Processes data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0c5-110">語法</span><span class="sxs-lookup"><span data-stu-id="fd0c5-110">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="fd0c5-111">參數</span><span class="sxs-lookup"><span data-stu-id="fd0c5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd0c5-112">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd0c5-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0c5-113">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="fd0c5-113">Type: **void\***</span></span>

<span data-ttu-id="fd0c5-114">要處理之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="fd0c5-114">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="fd0c5-115">*cBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd0c5-115">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0c5-116">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd0c5-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fd0c5-117">要處理的資料大小。</span><span class="sxs-lookup"><span data-stu-id="fd0c5-117">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd0c5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd0c5-118">Return value</span></span>

<span data-ttu-id="fd0c5-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd0c5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd0c5-120">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fd0c5-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0c5-121">備註</span><span class="sxs-lookup"><span data-stu-id="fd0c5-121">Remarks</span></span>

<span data-ttu-id="fd0c5-122">[**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fd0c5-122">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0c5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd0c5-123">Requirements</span></span>



| <span data-ttu-id="fd0c5-124">需求</span><span class="sxs-lookup"><span data-stu-id="fd0c5-124">Requirement</span></span> | <span data-ttu-id="fd0c5-125">值</span><span class="sxs-lookup"><span data-stu-id="fd0c5-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0c5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fd0c5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fd0c5-127"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0c5-127"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="fd0c5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd0c5-128">Library</span></span><br/> | <dl> <span data-ttu-id="fd0c5-129"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd0c5-129"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd0c5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd0c5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0c5-131">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="fd0c5-131">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="fd0c5-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="fd0c5-132">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

