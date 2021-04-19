---
description: Get \_ LoopbackMode 方法會取得多播回送模式。
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'IMulticastControl：： get_LoopbackMode 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976047"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="dba7f-103">IMulticastControl：： get \_ LoopbackMode 方法</span><span class="sxs-lookup"><span data-stu-id="dba7f-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="dba7f-104">\[**取得 \_LoopbackMode** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dba7f-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dba7f-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dba7f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dba7f-106">**Get \_ LoopbackMode** 方法會取得多播回送模式。</span><span class="sxs-lookup"><span data-stu-id="dba7f-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba7f-107">語法</span><span class="sxs-lookup"><span data-stu-id="dba7f-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="dba7f-108">參數</span><span class="sxs-lookup"><span data-stu-id="dba7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba7f-109">*pMode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dba7f-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dba7f-110">目前回送模式的 [**多播 \_ 回送 \_ 模式**](multicast-loopback-mode.md) 描述元指標。</span><span class="sxs-lookup"><span data-stu-id="dba7f-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba7f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dba7f-111">Return value</span></span>

<span data-ttu-id="dba7f-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dba7f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dba7f-113">值</span><span class="sxs-lookup"><span data-stu-id="dba7f-113">Value</span></span>                                                                                        | <span data-ttu-id="dba7f-114">意義</span><span class="sxs-lookup"><span data-stu-id="dba7f-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="dba7f-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dba7f-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dba7f-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="dba7f-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="dba7f-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dba7f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dba7f-118">*PMode* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="dba7f-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dba7f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dba7f-119">Requirements</span></span>



| <span data-ttu-id="dba7f-120">需求</span><span class="sxs-lookup"><span data-stu-id="dba7f-120">Requirement</span></span> | <span data-ttu-id="dba7f-121">值</span><span class="sxs-lookup"><span data-stu-id="dba7f-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dba7f-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="dba7f-122">TAPI version</span></span><br/> | <span data-ttu-id="dba7f-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="dba7f-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dba7f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dba7f-124">Header</span></span><br/>       | <dl> <span data-ttu-id="dba7f-125"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="dba7f-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="dba7f-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="dba7f-126">Library</span></span><br/>      | <dl> <span data-ttu-id="dba7f-127"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="dba7f-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dba7f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dba7f-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="dba7f-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dba7f-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dba7f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dba7f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba7f-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="dba7f-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




