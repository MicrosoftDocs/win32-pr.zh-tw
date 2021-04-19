---
title: IWMPLibrary isIdentical 方法
description: IsIdentical 方法會傳回一個值，這個值會指出提供的物件是否與目前的物件相同。
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- isIdentical 方法 Windows Media Player
- isIdentical 方法 Windows Media Player，IWMPLibrary 介面
- IWMPLibrary 介面 Windows Media Player，isIdentical 方法
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987836"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="ed61d-106">IWMPLibrary：： isIdentical 方法</span><span class="sxs-lookup"><span data-stu-id="ed61d-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="ed61d-107">**IsIdentical** 方法會傳回一個值，這個值會指出提供的物件是否與目前的物件相同。</span><span class="sxs-lookup"><span data-stu-id="ed61d-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed61d-108">語法</span><span class="sxs-lookup"><span data-stu-id="ed61d-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="ed61d-109">參數</span><span class="sxs-lookup"><span data-stu-id="ed61d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed61d-110">*pIWMPLibrary* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed61d-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed61d-111">**WMPLib IWMPLibrary** 介面，表示要與目前的物件比較的物件。</span><span class="sxs-lookup"><span data-stu-id="ed61d-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed61d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed61d-112">Return value</span></span>

<span data-ttu-id="ed61d-113">表示比較結果的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="ed61d-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="ed61d-114">值 **true** 表示物件相同。</span><span class="sxs-lookup"><span data-stu-id="ed61d-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed61d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed61d-115">Requirements</span></span>



| <span data-ttu-id="ed61d-116">需求</span><span class="sxs-lookup"><span data-stu-id="ed61d-116">Requirement</span></span> | <span data-ttu-id="ed61d-117">值</span><span class="sxs-lookup"><span data-stu-id="ed61d-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed61d-118">版本</span><span class="sxs-lookup"><span data-stu-id="ed61d-118">Version</span></span><br/>   | <span data-ttu-id="ed61d-119">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="ed61d-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ed61d-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="ed61d-120">Namespace</span></span><br/> | <span data-ttu-id="ed61d-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ed61d-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ed61d-122">組件</span><span class="sxs-lookup"><span data-stu-id="ed61d-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ed61d-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ed61d-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed61d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed61d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed61d-125">**IWMPLibrary 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ed61d-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





