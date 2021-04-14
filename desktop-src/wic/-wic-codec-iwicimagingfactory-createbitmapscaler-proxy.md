---
description: CreateBitmapScaler 方法的 Proxy 函式。
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: IWICImagingFactory_CreateBitmapScaler_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ac831427901de481d313833e4ca8459ccd333384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944991"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a><span data-ttu-id="cee79-103">IWICImagingFactory \_ CreateBitmapScaler \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="cee79-103">IWICImagingFactory\_CreateBitmapScaler\_Proxy function</span></span>

<span data-ttu-id="cee79-104">[**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="cee79-104">Proxy function for the [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee79-105">語法</span><span class="sxs-lookup"><span data-stu-id="cee79-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a><span data-ttu-id="cee79-106">參數</span><span class="sxs-lookup"><span data-stu-id="cee79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cee79-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cee79-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cee79-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="cee79-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="cee79-109">_ppIBitmapScaler \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cee79-109">_ppIBitmapScaler\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cee79-110">類型： **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span><span class="sxs-lookup"><span data-stu-id="cee79-110">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span></span>

<span data-ttu-id="cee79-111">接收新 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="cee79-111">A pointer that receives a pointer to a new [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cee79-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cee79-112">Return value</span></span>

<span data-ttu-id="cee79-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cee79-113">Type: **HRESULT**</span></span>

<span data-ttu-id="cee79-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cee79-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cee79-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cee79-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee79-116">備註</span><span class="sxs-lookup"><span data-stu-id="cee79-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cee79-117">需求</span><span class="sxs-lookup"><span data-stu-id="cee79-117">Requirements</span></span>



| <span data-ttu-id="cee79-118">需求</span><span class="sxs-lookup"><span data-stu-id="cee79-118">Requirement</span></span> | <span data-ttu-id="cee79-119">值</span><span class="sxs-lookup"><span data-stu-id="cee79-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee79-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cee79-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cee79-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cee79-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cee79-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cee79-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cee79-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cee79-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cee79-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cee79-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cee79-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cee79-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




