---
title: IWMPCdromBurn erase 方法
description: 清除方法會清除目前的 CD。
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- erase 方法 Windows Media Player
- IWMPCdromBurn 介面 Windows Media Player 清除方法
- IWMPCdromBurn 介面 Windows Media Player、erase 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998883"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="0ce35-106">IWMPCdromBurn：： erase 方法</span><span class="sxs-lookup"><span data-stu-id="0ce35-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="0ce35-107">**清除** 方法會清除目前的 CD。</span><span class="sxs-lookup"><span data-stu-id="0ce35-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce35-108">語法</span><span class="sxs-lookup"><span data-stu-id="0ce35-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="0ce35-109">參數</span><span class="sxs-lookup"><span data-stu-id="0ce35-109">Parameters</span></span>

<span data-ttu-id="0ce35-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0ce35-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ce35-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ce35-111">Return value</span></span>

<span data-ttu-id="0ce35-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0ce35-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce35-113">備註</span><span class="sxs-lookup"><span data-stu-id="0ce35-113">Remarks</span></span>

<span data-ttu-id="0ce35-114">如果磁片磁碟機中的光碟無法擦寫，則此方法將無法運作。</span><span class="sxs-lookup"><span data-stu-id="0ce35-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="0ce35-115">使用 [IWMPCdromBurn isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) 來判斷是否可以清除 CD。</span><span class="sxs-lookup"><span data-stu-id="0ce35-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce35-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ce35-116">Requirements</span></span>



| <span data-ttu-id="0ce35-117">需求</span><span class="sxs-lookup"><span data-stu-id="0ce35-117">Requirement</span></span> | <span data-ttu-id="0ce35-118">值</span><span class="sxs-lookup"><span data-stu-id="0ce35-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce35-119">版本</span><span class="sxs-lookup"><span data-stu-id="0ce35-119">Version</span></span><br/>   | <span data-ttu-id="0ce35-120">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="0ce35-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0ce35-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="0ce35-121">Namespace</span></span><br/> | <span data-ttu-id="0ce35-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ce35-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ce35-123">組件</span><span class="sxs-lookup"><span data-stu-id="0ce35-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ce35-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="0ce35-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce35-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ce35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce35-126">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0ce35-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





