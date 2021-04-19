---
title: IWMPCdromBurn burnState 屬性
description: BurnState 屬性會取得指出目前燒錄狀態的列舉值。
ms.assetid: 2bb543f9-9e4c-4425-99d6-ac89ef7f5807
keywords:
- burnState 屬性 Windows Media Player
- burnState 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，burnState 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnState
- IWMPCdromBurn.get_burnState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b1aa8ec39f032e8f130a75370131bd2894c64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994143"
---
# <a name="iwmpcdromburnburnstate-property"></a><span data-ttu-id="836f3-106">IWMPCdromBurn：： burnState 屬性</span><span class="sxs-lookup"><span data-stu-id="836f3-106">IWMPCdromBurn::burnState property</span></span>

<span data-ttu-id="836f3-107">**BurnState** 屬性會取得指出目前燒錄狀態的列舉值。</span><span class="sxs-lookup"><span data-stu-id="836f3-107">The **burnState** property gets an enumeration value that indicates the current burn state.</span></span>

<span data-ttu-id="836f3-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="836f3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="836f3-109">語法</span><span class="sxs-lookup"><span data-stu-id="836f3-109">Syntax</span></span>


```CSharp
public WMPBurnState burnState {get;}
```


```VB

Public ReadOnly Property burnState As WMPBurnState
```





## <a name="property-value"></a><span data-ttu-id="836f3-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="836f3-110">Property value</span></span>

<span data-ttu-id="836f3-111">**WMPLib** ，這是 **WMPBurnState** 列舉中表示目前狀態的值。</span><span class="sxs-lookup"><span data-stu-id="836f3-111">A **WMPLib.WMPBurnState** that is a value from the **WMPBurnState** enumeration that indicates the current state.</span></span>

## <a name="requirements"></a><span data-ttu-id="836f3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="836f3-112">Requirements</span></span>



| <span data-ttu-id="836f3-113">需求</span><span class="sxs-lookup"><span data-stu-id="836f3-113">Requirement</span></span> | <span data-ttu-id="836f3-114">值</span><span class="sxs-lookup"><span data-stu-id="836f3-114">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="836f3-115">版本</span><span class="sxs-lookup"><span data-stu-id="836f3-115">Version</span></span><br/>   | <span data-ttu-id="836f3-116">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="836f3-116">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="836f3-117">命名空間</span><span class="sxs-lookup"><span data-stu-id="836f3-117">Namespace</span></span><br/> | <span data-ttu-id="836f3-118">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="836f3-118">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="836f3-119">組件</span><span class="sxs-lookup"><span data-stu-id="836f3-119">Assembly</span></span><br/>  | <dl> <span data-ttu-id="836f3-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="836f3-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836f3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="836f3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836f3-122">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="836f3-122">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="836f3-123">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="836f3-123">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





