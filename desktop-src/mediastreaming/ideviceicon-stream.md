---
title: IDeviceIcon 資料流程方法
description: 以資料流程形式捕獲圖示。
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Stream 方法媒體串流 API
- Stream 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，Stream 方法
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315085"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="632d1-106">IDeviceIcon：： Stream 方法</span><span class="sxs-lookup"><span data-stu-id="632d1-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="632d1-107">以資料流程形式捕獲圖示。</span><span class="sxs-lookup"><span data-stu-id="632d1-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="632d1-108">語法</span><span class="sxs-lookup"><span data-stu-id="632d1-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="632d1-109">參數</span><span class="sxs-lookup"><span data-stu-id="632d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="632d1-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="632d1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="632d1-111">接收 [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) 的參考，該參考可用來取得影像資料。</span><span class="sxs-lookup"><span data-stu-id="632d1-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="632d1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="632d1-112">Return value</span></span>

<span data-ttu-id="632d1-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="632d1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="632d1-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="632d1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="632d1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="632d1-115">Return code</span></span>                                                                          | <span data-ttu-id="632d1-116">Description</span><span class="sxs-lookup"><span data-stu-id="632d1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="632d1-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="632d1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="632d1-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="632d1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="632d1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="632d1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632d1-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="632d1-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

