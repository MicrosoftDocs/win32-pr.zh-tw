---
title: 'WMDRMShutdown 函式 (Wmdrmsdk) '
description: WMDRMShutdown 函式會釋放 Windows Media DRM 用戶端擴充 Api 所使用的資源。
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- WMDRMShutdown 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982279"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="235a5-104">WMDRMShutdown 函式</span><span class="sxs-lookup"><span data-stu-id="235a5-104">WMDRMShutdown function</span></span>

<span data-ttu-id="235a5-105">**WMDRMShutdown** 函式會釋放 WINDOWS Media DRM 用戶端擴充 api 所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="235a5-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="235a5-106">語法</span><span class="sxs-lookup"><span data-stu-id="235a5-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="235a5-107">參數</span><span class="sxs-lookup"><span data-stu-id="235a5-107">Parameters</span></span>

<span data-ttu-id="235a5-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="235a5-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="235a5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="235a5-109">Return value</span></span>

<span data-ttu-id="235a5-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="235a5-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="235a5-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="235a5-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="235a5-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="235a5-112">Return code</span></span>                                                                          | <span data-ttu-id="235a5-113">Description</span><span class="sxs-lookup"><span data-stu-id="235a5-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="235a5-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="235a5-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="235a5-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="235a5-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="235a5-116">備註</span><span class="sxs-lookup"><span data-stu-id="235a5-116">Remarks</span></span>

<span data-ttu-id="235a5-117">若要避免記憶體流失，您必須針對 [**WMDRMStartup**](wmdrmstartup.md) 函式的每個呼叫呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="235a5-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="235a5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="235a5-118">Requirements</span></span>



| <span data-ttu-id="235a5-119">需求</span><span class="sxs-lookup"><span data-stu-id="235a5-119">Requirement</span></span> | <span data-ttu-id="235a5-120">值</span><span class="sxs-lookup"><span data-stu-id="235a5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="235a5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="235a5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="235a5-122"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="235a5-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="235a5-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="235a5-123">Library</span></span><br/> | <dl> <span data-ttu-id="235a5-124"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="235a5-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="235a5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="235a5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="235a5-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235a5-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235a5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="235a5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235a5-128">**函式**</span><span class="sxs-lookup"><span data-stu-id="235a5-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





