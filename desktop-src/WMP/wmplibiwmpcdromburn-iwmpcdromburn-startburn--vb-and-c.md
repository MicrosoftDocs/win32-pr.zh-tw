---
title: IWMPCdromBurn startBurn 方法
description: StartBurn 方法會燒錄 CD。
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- startBurn 方法 Windows Media Player
- startBurn 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，startBurn 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987193"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="91867-106">IWMPCdromBurn：： startBurn 方法</span><span class="sxs-lookup"><span data-stu-id="91867-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="91867-107">**StartBurn** 方法會燒錄 CD。</span><span class="sxs-lookup"><span data-stu-id="91867-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="91867-108">語法</span><span class="sxs-lookup"><span data-stu-id="91867-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="91867-109">參數</span><span class="sxs-lookup"><span data-stu-id="91867-109">Parameters</span></span>

<span data-ttu-id="91867-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="91867-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91867-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="91867-111">Return value</span></span>

<span data-ttu-id="91867-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="91867-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91867-113">備註</span><span class="sxs-lookup"><span data-stu-id="91867-113">Remarks</span></span>

<span data-ttu-id="91867-114">在呼叫這個方法之前， **burnstate** 的值應該是 WmpbsReady 或 wmpbsStopped。</span><span class="sxs-lookup"><span data-stu-id="91867-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="91867-115">如果 CD 光碟機不是燒錄機，或磁片磁碟機中的光碟無法寫入，此方法將無法運作。</span><span class="sxs-lookup"><span data-stu-id="91867-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="91867-116">使用 **isAvailable** 來判斷是否可以燒錄 CD。</span><span class="sxs-lookup"><span data-stu-id="91867-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="91867-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="91867-117">Requirements</span></span>



| <span data-ttu-id="91867-118">需求</span><span class="sxs-lookup"><span data-stu-id="91867-118">Requirement</span></span> | <span data-ttu-id="91867-119">值</span><span class="sxs-lookup"><span data-stu-id="91867-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91867-120">版本</span><span class="sxs-lookup"><span data-stu-id="91867-120">Version</span></span><br/>   | <span data-ttu-id="91867-121">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="91867-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="91867-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="91867-122">Namespace</span></span><br/> | <span data-ttu-id="91867-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="91867-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="91867-124">組件</span><span class="sxs-lookup"><span data-stu-id="91867-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="91867-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="91867-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91867-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91867-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91867-127">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91867-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91867-128">**IWMPCdromBurn. burnState (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91867-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91867-129">**IWMPCdromBurn. isAvailable (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91867-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91867-130">**IWMPCdromBurn. stopBurn (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91867-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





