---
description: Put \_ LoopbackMode 會設定多播回送模式。
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'IMulticastControl：:p ut_LoopbackMode 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993610"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="bac42-103">IMulticastControl：:p 的 \_ LoopbackMode 方法</span><span class="sxs-lookup"><span data-stu-id="bac42-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="bac42-104">\[**put \_LoopbackMode** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="bac42-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bac42-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="bac42-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bac42-106">**Put \_ LoopbackMode** 會設定多播回送模式。</span><span class="sxs-lookup"><span data-stu-id="bac42-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac42-107">語法</span><span class="sxs-lookup"><span data-stu-id="bac42-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="bac42-108">參數</span><span class="sxs-lookup"><span data-stu-id="bac42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac42-109">*模式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bac42-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac42-110">[**多播 \_新 \_**](multicast-loopback-mode.md) 回送模式的回送模式描述項。</span><span class="sxs-lookup"><span data-stu-id="bac42-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac42-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bac42-111">Return value</span></span>

<span data-ttu-id="bac42-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bac42-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bac42-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bac42-113">Return code</span></span>                                                                                  | <span data-ttu-id="bac42-114">Description</span><span class="sxs-lookup"><span data-stu-id="bac42-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="bac42-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bac42-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bac42-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="bac42-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="bac42-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bac42-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bac42-118">*模式* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="bac42-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bac42-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bac42-119">Requirements</span></span>



| <span data-ttu-id="bac42-120">需求</span><span class="sxs-lookup"><span data-stu-id="bac42-120">Requirement</span></span> | <span data-ttu-id="bac42-121">值</span><span class="sxs-lookup"><span data-stu-id="bac42-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bac42-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="bac42-122">TAPI version</span></span><br/> | <span data-ttu-id="bac42-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="bac42-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bac42-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bac42-124">Header</span></span><br/>       | <dl> <span data-ttu-id="bac42-125"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="bac42-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="bac42-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="bac42-126">Library</span></span><br/>      | <dl> <span data-ttu-id="bac42-127"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="bac42-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bac42-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bac42-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="bac42-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bac42-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bac42-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bac42-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac42-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="bac42-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




