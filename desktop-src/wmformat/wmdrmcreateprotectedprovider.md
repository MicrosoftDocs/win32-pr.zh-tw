---
title: 'WMDRMCreateProtectedProvider 函式 (Wmdrmsdk) '
description: WMDRMCreateProtectedProvider 函式會建立可建立其他 Windows Media DRM 用戶端擴充 Api 物件的 class factory。
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- WMDRMCreateProtectedProvider 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995185"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="66196-104">WMDRMCreateProtectedProvider 函式</span><span class="sxs-lookup"><span data-stu-id="66196-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="66196-105">**WMDRMCreateProtectedProvider** 函式會建立可建立其他 WINDOWS Media DRM 用戶端擴充 api 物件的 class factory。</span><span class="sxs-lookup"><span data-stu-id="66196-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="66196-106">此函式需要來自 Microsoft 的存根程式庫，並建立支援受保護 DRM 功能的物件。</span><span class="sxs-lookup"><span data-stu-id="66196-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="66196-107">語法</span><span class="sxs-lookup"><span data-stu-id="66196-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="66196-108">參數</span><span class="sxs-lookup"><span data-stu-id="66196-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66196-109">*ppDRMProvider* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="66196-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66196-110">接收新建立物件之 [**IWMDRMProvider**](iwmdrmprovider.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="66196-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66196-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="66196-111">Return value</span></span>

<span data-ttu-id="66196-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="66196-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66196-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="66196-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66196-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="66196-114">Return code</span></span>                                                                          | <span data-ttu-id="66196-115">Description</span><span class="sxs-lookup"><span data-stu-id="66196-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="66196-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="66196-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="66196-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="66196-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66196-118">備註</span><span class="sxs-lookup"><span data-stu-id="66196-118">Remarks</span></span>

<span data-ttu-id="66196-119">無。</span><span class="sxs-lookup"><span data-stu-id="66196-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="66196-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="66196-120">Requirements</span></span>



| <span data-ttu-id="66196-121">需求</span><span class="sxs-lookup"><span data-stu-id="66196-121">Requirement</span></span> | <span data-ttu-id="66196-122">值</span><span class="sxs-lookup"><span data-stu-id="66196-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66196-123">標頭</span><span class="sxs-lookup"><span data-stu-id="66196-123">Header</span></span><br/> | <dl> <span data-ttu-id="66196-124"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="66196-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66196-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66196-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66196-126">**函式**</span><span class="sxs-lookup"><span data-stu-id="66196-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="66196-127">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="66196-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 





