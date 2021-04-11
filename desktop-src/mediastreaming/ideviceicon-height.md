---
title: IDeviceIcon Height 方法
description: 抓取圖示的高度（以圖元為單位）。
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- Height 方法媒體串流 API
- Height 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，高度方法
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdba8d107cc844a29d215e5da49949595a8cd27a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023465"
---
# <a name="ideviceiconheight-method"></a><span data-ttu-id="06f49-106">IDeviceIcon：： Height 方法</span><span class="sxs-lookup"><span data-stu-id="06f49-106">IDeviceIcon::Height method</span></span>

<span data-ttu-id="06f49-107">抓取圖示的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="06f49-107">Retrieves the height of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f49-108">語法</span><span class="sxs-lookup"><span data-stu-id="06f49-108">Syntax</span></span>


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="06f49-109">參數</span><span class="sxs-lookup"><span data-stu-id="06f49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f49-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06f49-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06f49-111">接收圖示高度的指標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="06f49-111">Receives a pointer to the height of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f49-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="06f49-112">Return value</span></span>

<span data-ttu-id="06f49-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="06f49-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="06f49-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="06f49-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="06f49-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="06f49-115">Return code</span></span>                                                                          | <span data-ttu-id="06f49-116">Description</span><span class="sxs-lookup"><span data-stu-id="06f49-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="06f49-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="06f49-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="06f49-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="06f49-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="06f49-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06f49-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f49-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="06f49-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

