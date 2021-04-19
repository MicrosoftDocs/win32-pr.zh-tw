---
title: IWMPCdromBurn 標籤屬性
description: Label 屬性會取得 CD 磁片區標籤字串。
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- label 屬性 Windows Media Player
- label 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，label 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001592"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="781b1-106">IWMPCdromBurn：： label 屬性</span><span class="sxs-lookup"><span data-stu-id="781b1-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="781b1-107">*Label* 屬性會取得 CD 磁片區標籤字串。</span><span class="sxs-lookup"><span data-stu-id="781b1-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="781b1-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="781b1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="781b1-109">語法</span><span class="sxs-lookup"><span data-stu-id="781b1-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="781b1-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="781b1-110">Property value</span></span>

<span data-ttu-id="781b1-111">表示磁片區標籤字串的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="781b1-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="781b1-112">備註</span><span class="sxs-lookup"><span data-stu-id="781b1-112">Remarks</span></span>

<span data-ttu-id="781b1-113">由於 CD 標籤的儲存方式，CD 的標籤可能會比指定的磁片區標籤字串的長度還要短。</span><span class="sxs-lookup"><span data-stu-id="781b1-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="781b1-114">如果字串的長度超過 CD 標籤的最大長度，則會將文字截斷。</span><span class="sxs-lookup"><span data-stu-id="781b1-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="781b1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="781b1-115">Requirements</span></span>



| <span data-ttu-id="781b1-116">需求</span><span class="sxs-lookup"><span data-stu-id="781b1-116">Requirement</span></span> | <span data-ttu-id="781b1-117">值</span><span class="sxs-lookup"><span data-stu-id="781b1-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="781b1-118">版本</span><span class="sxs-lookup"><span data-stu-id="781b1-118">Version</span></span><br/>   | <span data-ttu-id="781b1-119">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="781b1-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="781b1-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="781b1-120">Namespace</span></span><br/> | <span data-ttu-id="781b1-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="781b1-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="781b1-122">組件</span><span class="sxs-lookup"><span data-stu-id="781b1-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="781b1-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="781b1-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781b1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="781b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781b1-125">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="781b1-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





