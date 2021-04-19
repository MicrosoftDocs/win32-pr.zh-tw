---
description: 從此集合移除 ICoNtextNode 物件。
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'ICoNtextNodes：： RemoveCoNtextNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972643"
---
# <a name="icontextnodesremovecontextnode-method"></a><span data-ttu-id="2d489-103">ICoNtextNodes：： RemoveCoNtextNode 方法</span><span class="sxs-lookup"><span data-stu-id="2d489-103">IContextNodes::RemoveContextNode method</span></span>

<span data-ttu-id="2d489-104">從此集合移除 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d489-104">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d489-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d489-105">Syntax</span></span>


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="2d489-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d489-107">*pCoNtextNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d489-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d489-108">要移除的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d489-108">The [**IContextNode**](icontextnode.md) object to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d489-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d489-109">Return value</span></span>

<span data-ttu-id="2d489-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="2d489-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d489-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d489-111">Requirements</span></span>



| <span data-ttu-id="2d489-112">需求</span><span class="sxs-lookup"><span data-stu-id="2d489-112">Requirement</span></span> | <span data-ttu-id="2d489-113">值</span><span class="sxs-lookup"><span data-stu-id="2d489-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d489-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d489-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2d489-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d489-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d489-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d489-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2d489-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d489-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2d489-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2d489-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d489-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="2d489-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2d489-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2d489-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d489-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d489-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2d489-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d489-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d489-123">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="2d489-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="2d489-124">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="2d489-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




