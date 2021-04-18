---
title: IDeviceIcon Width 方法
description: 抓取圖示的寬度（以圖元為單位）。
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Width 方法媒體串流 API
- Width 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，Width 方法
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b04f8c40cc209ccf1261af0fc2f6cdfd329db88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315082"
---
# <a name="ideviceiconwidth-method"></a><span data-ttu-id="65c90-106">IDeviceIcon：： Width 方法</span><span class="sxs-lookup"><span data-stu-id="65c90-106">IDeviceIcon::Width method</span></span>

<span data-ttu-id="65c90-107">抓取圖示的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="65c90-107">Retrieves the width of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c90-108">語法</span><span class="sxs-lookup"><span data-stu-id="65c90-108">Syntax</span></span>


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="65c90-109">參數</span><span class="sxs-lookup"><span data-stu-id="65c90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c90-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="65c90-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c90-111">接收圖示寬度的指標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="65c90-111">Receives a pointer to the width of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c90-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="65c90-112">Return value</span></span>

<span data-ttu-id="65c90-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="65c90-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="65c90-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="65c90-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="65c90-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="65c90-115">Return code</span></span>                                                                          | <span data-ttu-id="65c90-116">Description</span><span class="sxs-lookup"><span data-stu-id="65c90-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="65c90-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="65c90-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="65c90-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="65c90-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="65c90-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65c90-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c90-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="65c90-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

