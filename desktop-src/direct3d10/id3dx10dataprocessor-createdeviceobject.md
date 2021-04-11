---
description: 建立裝置物件。
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'ID3DX10DataProcessor：： CreateDeviceObject 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ed362f992ca2b9d3ce6e561e08e5fe7fd0bdbe3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196281"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="21bc7-103">ID3DX10DataProcessor：： CreateDeviceObject 方法</span><span class="sxs-lookup"><span data-stu-id="21bc7-103">ID3DX10DataProcessor::CreateDeviceObject method</span></span>

<span data-ttu-id="21bc7-104">建立裝置物件。</span><span class="sxs-lookup"><span data-stu-id="21bc7-104">Create a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bc7-105">語法</span><span class="sxs-lookup"><span data-stu-id="21bc7-105">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="21bc7-106">參數</span><span class="sxs-lookup"><span data-stu-id="21bc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bc7-107">*ppDataObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21bc7-107">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21bc7-108">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="21bc7-108">Type: **void\*\***</span></span>

<span data-ttu-id="21bc7-109">所建立裝置物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="21bc7-109">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21bc7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="21bc7-110">Return value</span></span>

<span data-ttu-id="21bc7-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21bc7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21bc7-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="21bc7-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21bc7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="21bc7-113">Requirements</span></span>



| <span data-ttu-id="21bc7-114">需求</span><span class="sxs-lookup"><span data-stu-id="21bc7-114">Requirement</span></span> | <span data-ttu-id="21bc7-115">值</span><span class="sxs-lookup"><span data-stu-id="21bc7-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21bc7-116">標頭</span><span class="sxs-lookup"><span data-stu-id="21bc7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="21bc7-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="21bc7-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="21bc7-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="21bc7-118">Library</span></span><br/> | <dl> <span data-ttu-id="21bc7-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21bc7-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21bc7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21bc7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bc7-121">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="21bc7-121">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="21bc7-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="21bc7-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




