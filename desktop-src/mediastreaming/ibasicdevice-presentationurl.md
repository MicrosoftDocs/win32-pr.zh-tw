---
title: IBasicDevice PresentationUrl 方法
description: 抓取裝置的簡報 URL。
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- PresentationUrl 方法媒體串流 API
- PresentationUrl 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，PresentationUrl 方法
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373000"
---
# <a name="ibasicdevicepresentationurl-method"></a><span data-ttu-id="df6fe-106">IBasicDevice：:P resentationUrl 方法</span><span class="sxs-lookup"><span data-stu-id="df6fe-106">IBasicDevice::PresentationUrl method</span></span>

<span data-ttu-id="df6fe-107">抓取裝置的簡報 URL。</span><span class="sxs-lookup"><span data-stu-id="df6fe-107">Retrieves the device s presentation URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6fe-108">語法</span><span class="sxs-lookup"><span data-stu-id="df6fe-108">Syntax</span></span>


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="df6fe-109">參數</span><span class="sxs-lookup"><span data-stu-id="df6fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6fe-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df6fe-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6fe-111">接收裝置展示 URL 的指標。</span><span class="sxs-lookup"><span data-stu-id="df6fe-111">Receives a pointer to the device s presentation URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6fe-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="df6fe-112">Return value</span></span>

<span data-ttu-id="df6fe-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="df6fe-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="df6fe-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="df6fe-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="df6fe-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="df6fe-115">Return code</span></span>                                                                          | <span data-ttu-id="df6fe-116">Description</span><span class="sxs-lookup"><span data-stu-id="df6fe-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="df6fe-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="df6fe-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="df6fe-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="df6fe-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="df6fe-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df6fe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6fe-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="df6fe-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





