---
title: IMediaRenderer IsImageSupported 方法
description: 抓取值，指出 DMR 是否能夠顯示影像。
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- IsImageSupported 方法媒體串流 API
- IsImageSupported 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，IsImageSupported 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967461"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="7daad-106">IMediaRenderer：： IsImageSupported 方法</span><span class="sxs-lookup"><span data-stu-id="7daad-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="7daad-107">抓取值，指出 DMR 是否能夠顯示影像。</span><span class="sxs-lookup"><span data-stu-id="7daad-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="7daad-108">語法</span><span class="sxs-lookup"><span data-stu-id="7daad-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="7daad-109">參數</span><span class="sxs-lookup"><span data-stu-id="7daad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7daad-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7daad-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7daad-111">布林值，如果 DMR 能夠顯示影像，則為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="7daad-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7daad-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7daad-112">Return value</span></span>

<span data-ttu-id="7daad-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="7daad-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7daad-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="7daad-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7daad-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7daad-115">Return code</span></span>                                                                          | <span data-ttu-id="7daad-116">Description</span><span class="sxs-lookup"><span data-stu-id="7daad-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7daad-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7daad-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7daad-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="7daad-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7daad-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7daad-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7daad-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="7daad-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





