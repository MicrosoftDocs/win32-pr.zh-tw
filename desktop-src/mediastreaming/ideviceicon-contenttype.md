---
title: IDeviceIcon ContentType 方法
description: 抓取圖示的內容類型。
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- ContentType 方法媒體串流 API
- ContentType 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，ContentType 方法
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842139"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="ee09e-106">IDeviceIcon：： ContentType 方法</span><span class="sxs-lookup"><span data-stu-id="ee09e-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="ee09e-107">抓取圖示的內容類型。</span><span class="sxs-lookup"><span data-stu-id="ee09e-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee09e-108">語法</span><span class="sxs-lookup"><span data-stu-id="ee09e-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="ee09e-109">參數</span><span class="sxs-lookup"><span data-stu-id="ee09e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee09e-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee09e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee09e-111">接收圖示內容類型的指標。</span><span class="sxs-lookup"><span data-stu-id="ee09e-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee09e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee09e-112">Return value</span></span>

<span data-ttu-id="ee09e-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ee09e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ee09e-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ee09e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ee09e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee09e-115">Return code</span></span>                                                                          | <span data-ttu-id="ee09e-116">Description</span><span class="sxs-lookup"><span data-stu-id="ee09e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ee09e-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ee09e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ee09e-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ee09e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ee09e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee09e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee09e-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="ee09e-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

