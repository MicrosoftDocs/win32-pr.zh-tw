---
title: IWMPSettings2 defaultAudioLanguage 屬性
description: DefaultAudioLanguage 屬性會取得 Windows Media Player 中指定之預設音訊語言 (LCID) 的地區設定識別碼。
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- defaultAudioLanguage 屬性 Windows Media Player
- defaultAudioLanguage 屬性 Windows Media Player，IWMPSettings2 介面
- IWMPSettings2 介面 Windows Media Player，defaultAudioLanguage 屬性
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983016"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a><span data-ttu-id="8a47a-106">IWMPSettings2：:d efaultAudioLanguage 屬性</span><span class="sxs-lookup"><span data-stu-id="8a47a-106">IWMPSettings2::defaultAudioLanguage property</span></span>

<span data-ttu-id="8a47a-107">**DefaultAudioLanguage** 屬性會取得 Windows Media Player 中指定之預設音訊語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a47a-107">The **defaultAudioLanguage** property gets the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>

<span data-ttu-id="8a47a-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8a47a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a47a-109">語法</span><span class="sxs-lookup"><span data-stu-id="8a47a-109">Syntax</span></span>


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="8a47a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="8a47a-110">Property value</span></span>

<span data-ttu-id="8a47a-111">為 LCID 的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="8a47a-111">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a47a-112">備註</span><span class="sxs-lookup"><span data-stu-id="8a47a-112">Remarks</span></span>

<span data-ttu-id="8a47a-113">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="8a47a-113">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a47a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a47a-114">Requirements</span></span>



| <span data-ttu-id="8a47a-115">需求</span><span class="sxs-lookup"><span data-stu-id="8a47a-115">Requirement</span></span> | <span data-ttu-id="8a47a-116">值</span><span class="sxs-lookup"><span data-stu-id="8a47a-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a47a-117">版本</span><span class="sxs-lookup"><span data-stu-id="8a47a-117">Version</span></span><br/>   | <span data-ttu-id="8a47a-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8a47a-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8a47a-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="8a47a-119">Namespace</span></span><br/> | <span data-ttu-id="8a47a-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8a47a-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8a47a-121">組件</span><span class="sxs-lookup"><span data-stu-id="8a47a-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a47a-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8a47a-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a47a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a47a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a47a-124">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a47a-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a47a-125">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a47a-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a47a-126">**IWMPSettings2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a47a-126">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





