---
title: 'WMDRMCreateProvider 函式 (Wmdrmsdk) '
description: WMDRMCreateProvider 函式會建立可建立其他 Windows Media DRM 用戶端擴充 Api 物件的 class factory。
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- WMDRMCreateProvider 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992825"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="ebfc3-104">WMDRMCreateProvider 函式</span><span class="sxs-lookup"><span data-stu-id="ebfc3-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="ebfc3-105">**WMDRMCreateProvider** 函式會建立可建立其他 WINDOWS Media DRM 用戶端擴充 api 物件的 class factory。</span><span class="sxs-lookup"><span data-stu-id="ebfc3-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="ebfc3-106">此函式不需要來自 Microsoft 的存根程式庫，並會建立不支援受保護 DRM 功能的物件。</span><span class="sxs-lookup"><span data-stu-id="ebfc3-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfc3-107">語法</span><span class="sxs-lookup"><span data-stu-id="ebfc3-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="ebfc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="ebfc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebfc3-109">*ppDRMProvider* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ebfc3-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebfc3-110">接收新建立物件之 [**IWMDRMProvider**](iwmdrmprovider.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ebfc3-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebfc3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebfc3-111">Return value</span></span>

<span data-ttu-id="ebfc3-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ebfc3-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ebfc3-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ebfc3-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ebfc3-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ebfc3-114">Return code</span></span>                                                                          | <span data-ttu-id="ebfc3-115">Description</span><span class="sxs-lookup"><span data-stu-id="ebfc3-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ebfc3-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc3-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ebfc3-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ebfc3-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ebfc3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebfc3-118">Requirements</span></span>



| <span data-ttu-id="ebfc3-119">需求</span><span class="sxs-lookup"><span data-stu-id="ebfc3-119">Requirement</span></span> | <span data-ttu-id="ebfc3-120">值</span><span class="sxs-lookup"><span data-stu-id="ebfc3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfc3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ebfc3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ebfc3-122"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc3-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebfc3-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebfc3-123">Library</span></span><br/> | <dl> <span data-ttu-id="ebfc3-124"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc3-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="ebfc3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ebfc3-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="ebfc3-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc3-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebfc3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebfc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfc3-128">**函式**</span><span class="sxs-lookup"><span data-stu-id="ebfc3-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="ebfc3-129">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="ebfc3-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





