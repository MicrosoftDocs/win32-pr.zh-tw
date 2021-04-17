---
description: 取得字型特性。
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font：： GetTextMetrics 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514617"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="17d15-103">ID3DX10Font：： GetTextMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="17d15-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="17d15-104">取得字型特性。</span><span class="sxs-lookup"><span data-stu-id="17d15-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d15-105">語法</span><span class="sxs-lookup"><span data-stu-id="17d15-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="17d15-106">參數</span><span class="sxs-lookup"><span data-stu-id="17d15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d15-107">*pTextMetrics* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17d15-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d15-108">類型： **TEXTMETRIC \***</span><span class="sxs-lookup"><span data-stu-id="17d15-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="17d15-109">[TEXTMETRIC](/previous-versions//ms534202(v=vs.85))結構的指標，其中包含字型屬性。</span><span class="sxs-lookup"><span data-stu-id="17d15-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="17d15-110">如果已定義 Unicode，函數會傳回 TEXTMETRICW 結構。</span><span class="sxs-lookup"><span data-stu-id="17d15-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="17d15-111">否則，函數會傳回 TEXTMETRICA 結構。</span><span class="sxs-lookup"><span data-stu-id="17d15-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d15-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="17d15-112">Return value</span></span>

<span data-ttu-id="17d15-113">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17d15-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17d15-114">如果函式成功則為非零，否則為 0。</span><span class="sxs-lookup"><span data-stu-id="17d15-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d15-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="17d15-115">Requirements</span></span>



| <span data-ttu-id="17d15-116">需求</span><span class="sxs-lookup"><span data-stu-id="17d15-116">Requirement</span></span> | <span data-ttu-id="17d15-117">值</span><span class="sxs-lookup"><span data-stu-id="17d15-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17d15-118">標頭</span><span class="sxs-lookup"><span data-stu-id="17d15-118">Header</span></span><br/>  | <dl> <span data-ttu-id="17d15-119"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="17d15-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="17d15-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="17d15-120">Library</span></span><br/> | <dl> <span data-ttu-id="17d15-121"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="17d15-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d15-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17d15-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d15-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="17d15-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="17d15-124">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="17d15-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
