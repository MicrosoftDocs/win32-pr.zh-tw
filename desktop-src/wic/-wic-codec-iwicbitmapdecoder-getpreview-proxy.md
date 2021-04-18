---
description: GetPreview 方法的 Proxy 函式。
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: IWICBitmapDecoder_GetPreview_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971389"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="b02f1-103">IWICBitmapDecoder \_ GetPreview \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="b02f1-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="b02f1-104">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="b02f1-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b02f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="b02f1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="b02f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="b02f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b02f1-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="b02f1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b02f1-108">類型： \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="b02f1-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="b02f1-109">這個 [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b02f1-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b02f1-110">*ppIBitmapSource* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b02f1-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b02f1-111">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="b02f1-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="b02f1-112">如果支援，則會接收預覽點陣圖指標的指標。</span><span class="sxs-lookup"><span data-stu-id="b02f1-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b02f1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b02f1-113">Return value</span></span>

<span data-ttu-id="b02f1-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b02f1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b02f1-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b02f1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b02f1-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b02f1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b02f1-117">備註</span><span class="sxs-lookup"><span data-stu-id="b02f1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b02f1-118">需求</span><span class="sxs-lookup"><span data-stu-id="b02f1-118">Requirements</span></span>



| <span data-ttu-id="b02f1-119">需求</span><span class="sxs-lookup"><span data-stu-id="b02f1-119">Requirement</span></span> | <span data-ttu-id="b02f1-120">值</span><span class="sxs-lookup"><span data-stu-id="b02f1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02f1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b02f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b02f1-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b02f1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b02f1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b02f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b02f1-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b02f1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b02f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b02f1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b02f1-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b02f1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




