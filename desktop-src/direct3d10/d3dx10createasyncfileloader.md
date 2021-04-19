---
description: 建立異步檔案載入器。
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: 'D3DX10CreateAsyncFileLoader 函式 (D3DX10Async) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000581"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="90798-103">D3DX10CreateAsyncFileLoader 函式</span><span class="sxs-lookup"><span data-stu-id="90798-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="90798-104">建立異步檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="90798-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="90798-105">語法</span><span class="sxs-lookup"><span data-stu-id="90798-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="90798-106">參數</span><span class="sxs-lookup"><span data-stu-id="90798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90798-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90798-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90798-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90798-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90798-109">要載入的檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="90798-109">The name of the file to load.</span></span> <span data-ttu-id="90798-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="90798-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="90798-111">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="90798-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="90798-112">*ppDataLoader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="90798-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90798-113">類型： **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="90798-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="90798-114">非同步資料載入器指標的位址 (參閱 [**ID3DX10DataLoader 介面**](id3dx10dataloader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="90798-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90798-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="90798-115">Return value</span></span>

<span data-ttu-id="90798-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90798-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90798-117">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="90798-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90798-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="90798-118">Requirements</span></span>



| <span data-ttu-id="90798-119">需求</span><span class="sxs-lookup"><span data-stu-id="90798-119">Requirement</span></span> | <span data-ttu-id="90798-120">值</span><span class="sxs-lookup"><span data-stu-id="90798-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90798-121">標頭</span><span class="sxs-lookup"><span data-stu-id="90798-121">Header</span></span><br/> | <dl> <span data-ttu-id="90798-122"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="90798-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90798-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90798-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90798-124">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="90798-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
