---
title: 'WMDRMStartup 函式 (Wmdrmsdk) '
description: WMDRMStartup 函式會初始化 Windows Media DRM 用戶端擴充 Api 所使用的資源。
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- WMDRMStartup 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993212"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="f8639-104">WMDRMStartup 函式</span><span class="sxs-lookup"><span data-stu-id="f8639-104">WMDRMStartup function</span></span>

<span data-ttu-id="f8639-105">**WMDRMStartup** 函式會初始化 WINDOWS Media DRM 用戶端擴充 api 所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="f8639-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8639-106">語法</span><span class="sxs-lookup"><span data-stu-id="f8639-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="f8639-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8639-107">Parameters</span></span>

<span data-ttu-id="f8639-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f8639-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8639-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8639-109">Return value</span></span>

<span data-ttu-id="f8639-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f8639-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f8639-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f8639-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f8639-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f8639-112">Return code</span></span>                                                                          | <span data-ttu-id="f8639-113">Description</span><span class="sxs-lookup"><span data-stu-id="f8639-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f8639-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f8639-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f8639-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f8639-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8639-116">備註</span><span class="sxs-lookup"><span data-stu-id="f8639-116">Remarks</span></span>

<span data-ttu-id="f8639-117">針對此函式的每個呼叫，您都必須呼叫 [**WMDRMShutdown**](wmdrmshutdown.md) 來釋放使用的資源。</span><span class="sxs-lookup"><span data-stu-id="f8639-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8639-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8639-118">Requirements</span></span>



| <span data-ttu-id="f8639-119">需求</span><span class="sxs-lookup"><span data-stu-id="f8639-119">Requirement</span></span> | <span data-ttu-id="f8639-120">值</span><span class="sxs-lookup"><span data-stu-id="f8639-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8639-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f8639-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f8639-122"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8639-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8639-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8639-123">Library</span></span><br/> | <dl> <span data-ttu-id="f8639-124"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8639-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8639-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f8639-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8639-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8639-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8639-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8639-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8639-128">**函式**</span><span class="sxs-lookup"><span data-stu-id="f8639-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





