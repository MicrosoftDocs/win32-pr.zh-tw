---
title: AxWindowsMediaPlayer. cdromCollection 屬性
description: CdromCollection 屬性會取得 IWMPCdromCollection 介面，以提供 CD 或 DVD 光碟機集合的存取權。
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- cdromCollection 屬性 Windows Media Player
- cdromCollection 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，cdromCollection 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983941"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="00c61-106">AxWindowsMediaPlayer. cdromCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="00c61-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="00c61-107">CdromCollection 屬性會取得 **IWMPCdromCollection** 介面，以提供 CD 或 DVD 光碟機集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="00c61-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="00c61-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="00c61-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c61-109">語法</span><span class="sxs-lookup"><span data-stu-id="00c61-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="00c61-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="00c61-110">Property value</span></span>

<span data-ttu-id="00c61-111">WMPLib IWMPCdromCollection 介面。</span><span class="sxs-lookup"><span data-stu-id="00c61-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="00c61-112">備註</span><span class="sxs-lookup"><span data-stu-id="00c61-112">Remarks</span></span>

<span data-ttu-id="00c61-113">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="00c61-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="00c61-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="00c61-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00c61-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="00c61-115">Requirements</span></span>



| <span data-ttu-id="00c61-116">需求</span><span class="sxs-lookup"><span data-stu-id="00c61-116">Requirement</span></span> | <span data-ttu-id="00c61-117">值</span><span class="sxs-lookup"><span data-stu-id="00c61-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c61-118">版本</span><span class="sxs-lookup"><span data-stu-id="00c61-118">Version</span></span><br/>   | <span data-ttu-id="00c61-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="00c61-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="00c61-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="00c61-120">Namespace</span></span><br/> | <span data-ttu-id="00c61-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="00c61-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="00c61-122">組件</span><span class="sxs-lookup"><span data-stu-id="00c61-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="00c61-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="00c61-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00c61-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00c61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c61-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="00c61-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00c61-126">**IWMPCdromCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="00c61-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00c61-127">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="00c61-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00c61-128">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="00c61-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





