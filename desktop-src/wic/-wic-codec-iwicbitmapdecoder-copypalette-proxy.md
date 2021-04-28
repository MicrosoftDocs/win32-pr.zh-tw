---
description: CopyPalette 方法的 IWICBitmapDecoder_CopyPalette_Proxy 函數 Proxy 函式。
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086356"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="8f1ff-103">IWICBitmapDecoder \_ CopyPalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="8f1ff-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="8f1ff-104">[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="8f1ff-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f1ff-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="8f1ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f1ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f1ff-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="8f1ff-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ff-108">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="8f1ff-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="8f1ff-109">這個 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="8f1ff-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="8f1ff-110">*pIPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f1ff-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ff-111">類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="8f1ff-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="8f1ff-112">要複製的影像調色板。</span><span class="sxs-lookup"><span data-stu-id="8f1ff-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f1ff-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f1ff-113">Return value</span></span>

<span data-ttu-id="8f1ff-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8f1ff-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8f1ff-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8f1ff-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f1ff-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8f1ff-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f1ff-117">備註</span><span class="sxs-lookup"><span data-stu-id="8f1ff-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8f1ff-118">需求</span><span class="sxs-lookup"><span data-stu-id="8f1ff-118">Requirements</span></span>



| <span data-ttu-id="8f1ff-119">需求</span><span class="sxs-lookup"><span data-stu-id="8f1ff-119">Requirement</span></span> | <span data-ttu-id="8f1ff-120">值</span><span class="sxs-lookup"><span data-stu-id="8f1ff-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1ff-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f1ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8f1ff-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f1ff-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8f1ff-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f1ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8f1ff-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f1ff-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8f1ff-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8f1ff-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f1ff-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f1ff-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




