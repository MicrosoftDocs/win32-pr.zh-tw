---
title: IBasicDevice 類型方法
description: 抓取列舉值，指出 DLNA 裝置的裝置類型。
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- 類型方法媒體串流 API
- 類型方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，類型方法
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383229"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="db2fa-106">IBasicDevice：： Type 方法</span><span class="sxs-lookup"><span data-stu-id="db2fa-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="db2fa-107">抓取列舉值，指出 DLNA 裝置的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="db2fa-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="db2fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="db2fa-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="db2fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="db2fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db2fa-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="db2fa-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db2fa-111">接收 [**DeviceTypes**](devicetypes.md) 值的指標。</span><span class="sxs-lookup"><span data-stu-id="db2fa-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db2fa-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="db2fa-112">Return value</span></span>

<span data-ttu-id="db2fa-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="db2fa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="db2fa-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="db2fa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="db2fa-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="db2fa-115">Return code</span></span>                                                                          | <span data-ttu-id="db2fa-116">Description</span><span class="sxs-lookup"><span data-stu-id="db2fa-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="db2fa-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="db2fa-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="db2fa-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="db2fa-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="db2fa-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db2fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db2fa-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="db2fa-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





