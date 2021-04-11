---
description: 抓取此集合中包含的 ICoNtextNode 物件數目。
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'ICoNtextNodes：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113368"
---
# <a name="icontextnodesgetcount-method"></a><span data-ttu-id="05f52-103">ICoNtextNodes：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="05f52-103">IContextNodes::GetCount method</span></span>

<span data-ttu-id="05f52-104">抓取此集合中包含的 [**ICoNtextNode**](icontextnode.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="05f52-104">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f52-105">語法</span><span class="sxs-lookup"><span data-stu-id="05f52-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="05f52-106">參數</span><span class="sxs-lookup"><span data-stu-id="05f52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f52-107">*pulCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05f52-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05f52-108">這個集合中所包含的 [**ICoNtextNode**](icontextnode.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="05f52-108">The number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f52-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="05f52-109">Return value</span></span>

<span data-ttu-id="05f52-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="05f52-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05f52-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f52-111">Requirements</span></span>



| <span data-ttu-id="05f52-112">需求</span><span class="sxs-lookup"><span data-stu-id="05f52-112">Requirement</span></span> | <span data-ttu-id="05f52-113">值</span><span class="sxs-lookup"><span data-stu-id="05f52-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f52-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05f52-114">Minimum supported client</span></span><br/> | <span data-ttu-id="05f52-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05f52-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05f52-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05f52-116">Minimum supported server</span></span><br/> | <span data-ttu-id="05f52-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="05f52-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05f52-118">標頭</span><span class="sxs-lookup"><span data-stu-id="05f52-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f52-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="05f52-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05f52-120">DLL</span><span class="sxs-lookup"><span data-stu-id="05f52-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f52-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f52-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05f52-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f52-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f52-123">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="05f52-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="05f52-124">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="05f52-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




