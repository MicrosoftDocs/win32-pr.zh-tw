---
description: 用於建立 IWICImagingFactory 的 Proxy 函數。
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986982"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="2e56b-103">WICCreateImagingFactory \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="2e56b-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="2e56b-104">用於建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="2e56b-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e56b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e56b-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="2e56b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e56b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e56b-107">*SDKVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e56b-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e56b-108">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="2e56b-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="2e56b-109">*ppIImagingFactory* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2e56b-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e56b-110">類型： **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e56b-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e56b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e56b-111">Return value</span></span>

<span data-ttu-id="2e56b-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e56b-112">Type: **HRESULT**</span></span>

<span data-ttu-id="2e56b-113">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2e56b-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e56b-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e56b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e56b-115">備註</span><span class="sxs-lookup"><span data-stu-id="2e56b-115">Remarks</span></span>

<span data-ttu-id="2e56b-116">此函式是協助程式，可為 Windows XP 所需的明確 DLL 連結建立 WIC factory。</span><span class="sxs-lookup"><span data-stu-id="2e56b-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="2e56b-117">在正常使用方式下，您會改為使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (請參閱 [WIC API class](./-wic-api.md#class-factories) factory) ，因為這一律包含在所有較新版本的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="2e56b-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e56b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e56b-118">Requirements</span></span>



| <span data-ttu-id="2e56b-119">需求</span><span class="sxs-lookup"><span data-stu-id="2e56b-119">Requirement</span></span> | <span data-ttu-id="2e56b-120">值</span><span class="sxs-lookup"><span data-stu-id="2e56b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e56b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e56b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e56b-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e56b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2e56b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e56b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e56b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e56b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2e56b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2e56b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e56b-126"><dt>Windowscodecs.dll;</dt><dt>windowscodecs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e56b-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

