---
title: IDWriteTextLayout DetermineMinWidth 方法
description: 判斷配置可設定的最小可能寬度，而不會在整個單字的字元之間進行緊急中斷。
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- DetermineMinWidth 方法直接寫入
- DetermineMinWidth 方法 Direct Write，IDWriteTextLayout 介面
- IDWriteTextLayout 介面 Direct Write，DetermineMinWidth 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981647"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="8d167-106">IDWriteTextLayout：:D etermineMinWidth 方法</span><span class="sxs-lookup"><span data-stu-id="8d167-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="8d167-107">判斷配置可設定的最小可能寬度，而不會在整個單字的字元之間進行緊急中斷。</span><span class="sxs-lookup"><span data-stu-id="8d167-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d167-108">語法</span><span class="sxs-lookup"><span data-stu-id="8d167-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8d167-109">參數</span><span class="sxs-lookup"><span data-stu-id="8d167-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d167-110">*minWidth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8d167-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d167-111">類型： **FLOAT \***</span><span class="sxs-lookup"><span data-stu-id="8d167-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="8d167-112">寬度下限。</span><span class="sxs-lookup"><span data-stu-id="8d167-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d167-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d167-113">Return value</span></span>

<span data-ttu-id="8d167-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d167-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8d167-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8d167-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d167-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8d167-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d167-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d167-117">Requirements</span></span>



| <span data-ttu-id="8d167-118">需求</span><span class="sxs-lookup"><span data-stu-id="8d167-118">Requirement</span></span> | <span data-ttu-id="8d167-119">值</span><span class="sxs-lookup"><span data-stu-id="8d167-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d167-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d167-120">Library</span></span><br/> | <dl> <span data-ttu-id="8d167-121"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d167-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d167-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8d167-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d167-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d167-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d167-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d167-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d167-125">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="8d167-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="8d167-126">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="8d167-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

