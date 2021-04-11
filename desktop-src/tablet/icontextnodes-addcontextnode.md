---
description: 將 ICoNtextNode 物件加入至此集合。
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: 'ICoNtextNodes：： AddCoNtextNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.AddContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 18a7438c09fb2a850637bbae549ada61c37fb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113369"
---
# <a name="icontextnodesaddcontextnode-method"></a><span data-ttu-id="399a1-103">ICoNtextNodes：： AddCoNtextNode 方法</span><span class="sxs-lookup"><span data-stu-id="399a1-103">IContextNodes::AddContextNode method</span></span>

<span data-ttu-id="399a1-104">將 [**ICoNtextNode**](icontextnode.md) 物件加入至此集合。</span><span class="sxs-lookup"><span data-stu-id="399a1-104">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="399a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="399a1-105">Syntax</span></span>


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="399a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="399a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="399a1-107">*pCoNtextNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="399a1-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="399a1-108">要加入的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="399a1-108">The [**IContextNode**](icontextnode.md) object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="399a1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="399a1-109">Return value</span></span>

<span data-ttu-id="399a1-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="399a1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="399a1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="399a1-111">Requirements</span></span>



| <span data-ttu-id="399a1-112">需求</span><span class="sxs-lookup"><span data-stu-id="399a1-112">Requirement</span></span> | <span data-ttu-id="399a1-113">值</span><span class="sxs-lookup"><span data-stu-id="399a1-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399a1-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="399a1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="399a1-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="399a1-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="399a1-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="399a1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="399a1-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="399a1-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="399a1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="399a1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="399a1-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="399a1-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="399a1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="399a1-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="399a1-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="399a1-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="399a1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="399a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399a1-123">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="399a1-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="399a1-124">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="399a1-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




