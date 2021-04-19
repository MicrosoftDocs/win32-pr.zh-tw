---
title: AxWindowsMediaPlayer. mediaCollection 屬性
description: MediaCollection 屬性會取得 IWMPMediaCollection 介面，以提供一種方式來組織大型的媒體專案集合。
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- mediaCollection 屬性 Windows Media Player
- mediaCollection 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，mediaCollection 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995448"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="5f30f-106">AxWindowsMediaPlayer. mediaCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="5f30f-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="5f30f-107">MediaCollection 屬性會取得 **IWMPMediaCollection** 介面，以提供一種方式來組織大型的媒體專案集合。</span><span class="sxs-lookup"><span data-stu-id="5f30f-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="5f30f-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5f30f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f30f-109">語法</span><span class="sxs-lookup"><span data-stu-id="5f30f-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="5f30f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5f30f-110">Property value</span></span>

<span data-ttu-id="5f30f-111">WMPLib IWMPMediaCollection 介面，指向媒體專案的集合。</span><span class="sxs-lookup"><span data-stu-id="5f30f-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f30f-112">備註</span><span class="sxs-lookup"><span data-stu-id="5f30f-112">Remarks</span></span>

<span data-ttu-id="5f30f-113">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="5f30f-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5f30f-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="5f30f-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f30f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f30f-115">Requirements</span></span>



| <span data-ttu-id="5f30f-116">需求</span><span class="sxs-lookup"><span data-stu-id="5f30f-116">Requirement</span></span> | <span data-ttu-id="5f30f-117">值</span><span class="sxs-lookup"><span data-stu-id="5f30f-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f30f-118">版本</span><span class="sxs-lookup"><span data-stu-id="5f30f-118">Version</span></span><br/>   | <span data-ttu-id="5f30f-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="5f30f-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5f30f-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="5f30f-120">Namespace</span></span><br/> | <span data-ttu-id="5f30f-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5f30f-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5f30f-122">組件</span><span class="sxs-lookup"><span data-stu-id="5f30f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5f30f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="5f30f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f30f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f30f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f30f-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5f30f-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5f30f-126">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5f30f-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5f30f-127">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5f30f-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5f30f-128">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5f30f-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





