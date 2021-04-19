---
title: IWMPMedia2 Error 屬性
description: 如果媒體專案有錯誤條件，錯誤屬性會取得 IWMPErrorItem 介面。
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Error 屬性 Windows Media Player
- Error 屬性 Windows Media Player，IWMPMedia2 介面
- IWMPMedia2 介面 Windows Media Player，Error 屬性
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985947"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="47c70-106">IWMPMedia2：： Error 屬性</span><span class="sxs-lookup"><span data-stu-id="47c70-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="47c70-107">如果媒體專案有錯誤條件， **錯誤** 屬性會取得 **IWMPErrorItem** 介面。</span><span class="sxs-lookup"><span data-stu-id="47c70-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="47c70-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="47c70-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c70-109">語法</span><span class="sxs-lookup"><span data-stu-id="47c70-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="47c70-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="47c70-110">Property value</span></span>

<span data-ttu-id="47c70-111">**WMPLib IWMPErrorItem** 介面，可讓您存取錯誤狀況的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="47c70-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c70-112">備註</span><span class="sxs-lookup"><span data-stu-id="47c70-112">Remarks</span></span>

<span data-ttu-id="47c70-113">如果無法播放媒體專案，這個屬性會取得 **IWMPErrorItem** 介面，其中包含所發生問題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="47c70-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c70-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="47c70-114">Requirements</span></span>



| <span data-ttu-id="47c70-115">需求</span><span class="sxs-lookup"><span data-stu-id="47c70-115">Requirement</span></span> | <span data-ttu-id="47c70-116">值</span><span class="sxs-lookup"><span data-stu-id="47c70-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c70-117">版本</span><span class="sxs-lookup"><span data-stu-id="47c70-117">Version</span></span><br/>   | <span data-ttu-id="47c70-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="47c70-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="47c70-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="47c70-119">Namespace</span></span><br/> | <span data-ttu-id="47c70-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="47c70-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="47c70-121">組件</span><span class="sxs-lookup"><span data-stu-id="47c70-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="47c70-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="47c70-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c70-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47c70-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c70-124">**IWMPErrorItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="47c70-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="47c70-125">**IWMPMedia2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="47c70-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





