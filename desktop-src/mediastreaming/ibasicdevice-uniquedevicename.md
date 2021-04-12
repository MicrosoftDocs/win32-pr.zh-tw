---
title: IBasicDevice UniqueDeviceName 方法
description: 抓取裝置的唯一裝置名稱 (UDN) 。
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- UniqueDeviceName 方法媒體串流 API
- UniqueDeviceName 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，UniqueDeviceName 方法
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372988"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="29ba7-106">IBasicDevice：： UniqueDeviceName 方法</span><span class="sxs-lookup"><span data-stu-id="29ba7-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="29ba7-107">抓取裝置的唯一裝置名稱 (UDN) 。</span><span class="sxs-lookup"><span data-stu-id="29ba7-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="29ba7-108">語法</span><span class="sxs-lookup"><span data-stu-id="29ba7-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="29ba7-109">參數</span><span class="sxs-lookup"><span data-stu-id="29ba7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ba7-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="29ba7-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29ba7-111">接收裝置 s 模型 UDN 的指標。</span><span class="sxs-lookup"><span data-stu-id="29ba7-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ba7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="29ba7-112">Return value</span></span>

<span data-ttu-id="29ba7-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="29ba7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="29ba7-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="29ba7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="29ba7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="29ba7-115">Return code</span></span>                                                                          | <span data-ttu-id="29ba7-116">Description</span><span class="sxs-lookup"><span data-stu-id="29ba7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="29ba7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="29ba7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="29ba7-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="29ba7-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="29ba7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29ba7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ba7-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="29ba7-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





