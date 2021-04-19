---
title: AxWindowsMediaPlayer。 status 屬性
description: Status 屬性會取得值，指出 Windows Media Player 的狀態。
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- status 屬性 Windows Media Player
- status 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，status 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983047"
---
# <a name="axwindowsmediaplayerstatus-property"></a><span data-ttu-id="4c739-106">AxWindowsMediaPlayer。 status 屬性</span><span class="sxs-lookup"><span data-stu-id="4c739-106">AxWindowsMediaPlayer.status property</span></span>

<span data-ttu-id="4c739-107">Status 屬性會取得值，指出 Windows Media Player 的狀態。</span><span class="sxs-lookup"><span data-stu-id="4c739-107">The status property gets a value indicating the status of Windows Media Player.</span></span>

<span data-ttu-id="4c739-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4c739-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c739-109">語法</span><span class="sxs-lookup"><span data-stu-id="4c739-109">Syntax</span></span>


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a><span data-ttu-id="4c739-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="4c739-110">Property value</span></span>

<span data-ttu-id="4c739-111">表示狀態的 System.string。</span><span class="sxs-lookup"><span data-stu-id="4c739-111">The System.String that is the status.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c739-112">備註</span><span class="sxs-lookup"><span data-stu-id="4c739-112">Remarks</span></span>

<span data-ttu-id="4c739-113">這個屬性中包含的值隨時可能會變更，而且僅供顯示之用。</span><span class="sxs-lookup"><span data-stu-id="4c739-113">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="4c739-114">AxWindowsMediaPlayer。每當這個屬性變更值時，就會引發 **StatusChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="4c739-114">The AxWindowsMediaPlayer.**StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c739-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c739-115">Requirements</span></span>



| <span data-ttu-id="4c739-116">需求</span><span class="sxs-lookup"><span data-stu-id="4c739-116">Requirement</span></span> | <span data-ttu-id="4c739-117">值</span><span class="sxs-lookup"><span data-stu-id="4c739-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c739-118">版本</span><span class="sxs-lookup"><span data-stu-id="4c739-118">Version</span></span><br/>   | <span data-ttu-id="4c739-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4c739-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4c739-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c739-120">Namespace</span></span><br/> | <span data-ttu-id="4c739-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c739-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4c739-122">組件</span><span class="sxs-lookup"><span data-stu-id="4c739-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c739-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4c739-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c739-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c739-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c739-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4c739-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4c739-126">**AxWindowsMediaPlayer StatusChange 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4c739-126">**AxWindowsMediaPlayer.StatusChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





