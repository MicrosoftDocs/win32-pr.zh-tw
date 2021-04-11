---
description: 抓取這個 ICoNtextNode 的人們看得懂的型別名稱。
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'ICoNtextNode：： GetTypeName 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113376"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="41322-103">ICoNtextNode：： GetTypeName 方法</span><span class="sxs-lookup"><span data-stu-id="41322-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="41322-104">抓取這個 [**ICoNtextNode**](icontextnode.md)的人們看得懂的型別名稱。</span><span class="sxs-lookup"><span data-stu-id="41322-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41322-105">語法</span><span class="sxs-lookup"><span data-stu-id="41322-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="41322-106">參數</span><span class="sxs-lookup"><span data-stu-id="41322-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41322-107">*pbstrCoNtextNodeType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="41322-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41322-108">這個 [**ICoNtextNode**](icontextnode.md)的人們可讀取型別名稱。</span><span class="sxs-lookup"><span data-stu-id="41322-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41322-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="41322-109">Return value</span></span>

<span data-ttu-id="41322-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="41322-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41322-111">備註</span><span class="sxs-lookup"><span data-stu-id="41322-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="41322-112">若要避免記憶體流失， [](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) \* 當您不再需要使用字串時，請在 *pbstrCoNtextNodeType* 上呼叫 SysFreeString。</span><span class="sxs-lookup"><span data-stu-id="41322-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="41322-113">例如，這個方法會將筆墨單位元組點的 *pbstrCoNtextNodeType* 設定為 "InkWordNode"， (查看 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。</span><span class="sxs-lookup"><span data-stu-id="41322-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="41322-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="41322-114">Requirements</span></span>



| <span data-ttu-id="41322-115">需求</span><span class="sxs-lookup"><span data-stu-id="41322-115">Requirement</span></span> | <span data-ttu-id="41322-116">值</span><span class="sxs-lookup"><span data-stu-id="41322-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41322-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41322-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41322-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41322-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="41322-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41322-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41322-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="41322-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="41322-121">標頭</span><span class="sxs-lookup"><span data-stu-id="41322-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41322-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="41322-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="41322-123">DLL</span><span class="sxs-lookup"><span data-stu-id="41322-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41322-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41322-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="41322-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41322-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41322-126">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="41322-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="41322-127">**ICoNtextNode：： GetType**</span><span class="sxs-lookup"><span data-stu-id="41322-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="41322-128">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="41322-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="41322-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="41322-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

