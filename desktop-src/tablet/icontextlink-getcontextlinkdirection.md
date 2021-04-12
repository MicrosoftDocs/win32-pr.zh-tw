---
description: 抓取這個 ICoNtextLink 所代表的關聯性類型。
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'ICoNtextLink：： GetCoNtextLinkDirection 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191417"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="3e3ef-103">ICoNtextLink：： GetCoNtextLinkDirection 方法</span><span class="sxs-lookup"><span data-stu-id="3e3ef-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="3e3ef-104">抓取這個 [**ICoNtextLink**](icontextlink.md) 所代表的關聯性類型。</span><span class="sxs-lookup"><span data-stu-id="3e3ef-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e3ef-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="3e3ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e3ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e3ef-107">*pCoNtextLinkDirection* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3e3ef-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3ef-108">此 [**ICoNtextLink**](icontextlink.md) 所代表的方向。</span><span class="sxs-lookup"><span data-stu-id="3e3ef-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e3ef-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e3ef-109">Return value</span></span>

<span data-ttu-id="3e3ef-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="3e3ef-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3ef-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e3ef-111">Requirements</span></span>



| <span data-ttu-id="3e3ef-112">需求</span><span class="sxs-lookup"><span data-stu-id="3e3ef-112">Requirement</span></span> | <span data-ttu-id="3e3ef-113">值</span><span class="sxs-lookup"><span data-stu-id="3e3ef-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3ef-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e3ef-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3e3ef-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e3ef-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e3ef-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e3ef-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3e3ef-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e3ef-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3e3ef-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3e3ef-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e3ef-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3e3ef-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e3ef-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3e3ef-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e3ef-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e3ef-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3e3ef-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e3ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3ef-123">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="3e3ef-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="3e3ef-124">**CoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="3e3ef-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="3e3ef-125">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="3e3ef-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




