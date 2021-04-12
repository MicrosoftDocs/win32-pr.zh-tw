---
title: IBasicDevice SerialNumber 方法
description: 抓取裝置序號。
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- SerialNumber 方法媒體串流 API
- SerialNumber 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，SerialNumber 方法
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312488"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="3c3d4-106">IBasicDevice：： SerialNumber 方法</span><span class="sxs-lookup"><span data-stu-id="3c3d4-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="3c3d4-107">抓取裝置序號。</span><span class="sxs-lookup"><span data-stu-id="3c3d4-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3d4-108">語法</span><span class="sxs-lookup"><span data-stu-id="3c3d4-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="3c3d4-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c3d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3d4-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c3d4-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3d4-111">接收裝置序號的指標。</span><span class="sxs-lookup"><span data-stu-id="3c3d4-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3d4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c3d4-112">Return value</span></span>

<span data-ttu-id="3c3d4-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3c3d4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3c3d4-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3c3d4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3c3d4-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3c3d4-115">Return code</span></span>                                                                          | <span data-ttu-id="3c3d4-116">Description</span><span class="sxs-lookup"><span data-stu-id="3c3d4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3c3d4-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3c3d4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3c3d4-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3c3d4-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="3c3d4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c3d4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3d4-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="3c3d4-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





