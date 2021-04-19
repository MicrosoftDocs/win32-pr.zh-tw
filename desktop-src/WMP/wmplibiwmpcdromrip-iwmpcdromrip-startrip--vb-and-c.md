---
title: IWMPCdromRip startRip 方法
description: StartRip 方法會將 CD 翻錄。
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- startRip 方法 Windows Media Player
- startRip 方法 Windows Media Player，IWMPCdromRip 介面
- IWMPCdromRip 介面 Windows Media Player，startRip 方法
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994341"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="4c441-106">IWMPCdromRip：： startRip 方法</span><span class="sxs-lookup"><span data-stu-id="4c441-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="4c441-107">**StartRip** 方法會將 CD 翻錄。</span><span class="sxs-lookup"><span data-stu-id="4c441-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c441-108">語法</span><span class="sxs-lookup"><span data-stu-id="4c441-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="4c441-109">參數</span><span class="sxs-lookup"><span data-stu-id="4c441-109">Parameters</span></span>

<span data-ttu-id="4c441-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4c441-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c441-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c441-111">Return value</span></span>

<span data-ttu-id="4c441-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4c441-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c441-113">備註</span><span class="sxs-lookup"><span data-stu-id="4c441-113">Remarks</span></span>

<span data-ttu-id="4c441-114">使用 **IWMPCdromRip** 介面來將 CD 翻錄，與使用 Windows Media Player 使用者介面來將音樂翻錄的效果相同。</span><span class="sxs-lookup"><span data-stu-id="4c441-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="4c441-115">已翻錄的內容會根據使用者的喜好設定自動新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="4c441-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="4c441-116">如需 CD 翻錄使用者喜好設定的詳細資訊，請參閱 Windows Media Player 說明中的「從 Cd 翻錄音樂」。</span><span class="sxs-lookup"><span data-stu-id="4c441-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c441-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c441-117">Requirements</span></span>



| <span data-ttu-id="4c441-118">需求</span><span class="sxs-lookup"><span data-stu-id="4c441-118">Requirement</span></span> | <span data-ttu-id="4c441-119">值</span><span class="sxs-lookup"><span data-stu-id="4c441-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c441-120">版本</span><span class="sxs-lookup"><span data-stu-id="4c441-120">Version</span></span><br/>   | <span data-ttu-id="4c441-121">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="4c441-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="4c441-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c441-122">Namespace</span></span><br/> | <span data-ttu-id="4c441-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c441-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4c441-124">組件</span><span class="sxs-lookup"><span data-stu-id="4c441-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c441-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4c441-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c441-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c441-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c441-127">**IWMPCdromRip 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4c441-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4c441-128">**IWMPCdromRip.stopRip**</span><span class="sxs-lookup"><span data-stu-id="4c441-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4c441-129">**將 CD 翻錄**</span><span class="sxs-lookup"><span data-stu-id="4c441-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





