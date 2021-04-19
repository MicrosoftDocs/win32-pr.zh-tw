---
title: AxWindowsMediaPlayer. openState 屬性
description: OpenState 屬性會取得指出內容來源狀態的列舉值。
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- openState 屬性 Windows Media Player
- openState 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，openState 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977454"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="6058e-106">AxWindowsMediaPlayer. openState 屬性</span><span class="sxs-lookup"><span data-stu-id="6058e-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="6058e-107">OpenState 屬性會取得指出內容來源狀態的列舉值。</span><span class="sxs-lookup"><span data-stu-id="6058e-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="6058e-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6058e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6058e-109">語法</span><span class="sxs-lookup"><span data-stu-id="6058e-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="6058e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6058e-110">Property value</span></span>

<span data-ttu-id="6058e-111">WMPLib. WMPOpenState 列舉值。</span><span class="sxs-lookup"><span data-stu-id="6058e-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6058e-112">備註</span><span class="sxs-lookup"><span data-stu-id="6058e-112">Remarks</span></span>

<span data-ttu-id="6058e-113">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="6058e-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="6058e-114">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="6058e-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="6058e-115">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6058e-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="6058e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6058e-116">Requirements</span></span>



| <span data-ttu-id="6058e-117">需求</span><span class="sxs-lookup"><span data-stu-id="6058e-117">Requirement</span></span> | <span data-ttu-id="6058e-118">值</span><span class="sxs-lookup"><span data-stu-id="6058e-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6058e-119">版本</span><span class="sxs-lookup"><span data-stu-id="6058e-119">Version</span></span><br/>   | <span data-ttu-id="6058e-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6058e-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6058e-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="6058e-121">Namespace</span></span><br/> | <span data-ttu-id="6058e-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6058e-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6058e-123">組件</span><span class="sxs-lookup"><span data-stu-id="6058e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6058e-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6058e-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6058e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6058e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6058e-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6058e-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6058e-127">**AxWindowsMediaPlayer. OpenStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="6058e-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="6058e-128">**WMPLib.WMPOpenState**</span><span class="sxs-lookup"><span data-stu-id="6058e-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





