---
title: IWMPStringCollection2 isIdentical 方法
description: IsIdentical 方法會傳回值，指出提供的介面所表示的物件是否與目前的介面相同。
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- isIdentical 方法 Windows Media Player
- isIdentical 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，isIdentical 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000936"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="16f7d-106">IWMPStringCollection2：： isIdentical 方法</span><span class="sxs-lookup"><span data-stu-id="16f7d-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="16f7d-107">**IsIdentical** 方法會傳回值，指出提供的介面所表示的物件是否與目前的介面相同。</span><span class="sxs-lookup"><span data-stu-id="16f7d-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f7d-108">語法</span><span class="sxs-lookup"><span data-stu-id="16f7d-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="16f7d-109">參數</span><span class="sxs-lookup"><span data-stu-id="16f7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f7d-110">*pIWMPStringCollection2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16f7d-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f7d-111">**WMPLib. IWMPStringCollection2** 介面，表示要與目前物件比較的物件。</span><span class="sxs-lookup"><span data-stu-id="16f7d-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f7d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="16f7d-112">Return value</span></span>

<span data-ttu-id="16f7d-113">此為比較結果的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="16f7d-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="16f7d-114">**True** 值表示字串集合物件相同。</span><span class="sxs-lookup"><span data-stu-id="16f7d-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f7d-115">備註</span><span class="sxs-lookup"><span data-stu-id="16f7d-115">Remarks</span></span>

<span data-ttu-id="16f7d-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="16f7d-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="16f7d-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="16f7d-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16f7d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="16f7d-118">Requirements</span></span>



| <span data-ttu-id="16f7d-119">需求</span><span class="sxs-lookup"><span data-stu-id="16f7d-119">Requirement</span></span> | <span data-ttu-id="16f7d-120">值</span><span class="sxs-lookup"><span data-stu-id="16f7d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f7d-121">版本</span><span class="sxs-lookup"><span data-stu-id="16f7d-121">Version</span></span><br/>   | <span data-ttu-id="16f7d-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="16f7d-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="16f7d-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="16f7d-123">Namespace</span></span><br/> | <span data-ttu-id="16f7d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="16f7d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="16f7d-125">組件</span><span class="sxs-lookup"><span data-stu-id="16f7d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16f7d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="16f7d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f7d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16f7d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f7d-128">**IWMPStringCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="16f7d-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





