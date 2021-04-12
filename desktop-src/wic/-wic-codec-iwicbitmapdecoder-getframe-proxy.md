---
description: GetFrame 方法的 Proxy 函式。
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: IWICBitmapDecoder_GetFrame_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318267"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="00545-103">IWICBitmapDecoder \_ GetFrame \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="00545-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="00545-104">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="00545-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00545-105">語法</span><span class="sxs-lookup"><span data-stu-id="00545-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="00545-106">參數</span><span class="sxs-lookup"><span data-stu-id="00545-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00545-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="00545-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00545-108">類型： \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="00545-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="00545-109">這個 [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="00545-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="00545-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00545-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00545-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="00545-111">Type: **UINT**</span></span>

<span data-ttu-id="00545-112">要取出的特定框架。</span><span class="sxs-lookup"><span data-stu-id="00545-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="00545-113">*ppIBitmapFrame* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00545-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00545-114">類型： **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="00545-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="00545-115">接收 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="00545-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00545-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="00545-116">Return value</span></span>

<span data-ttu-id="00545-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00545-117">Type: **HRESULT**</span></span>

<span data-ttu-id="00545-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="00545-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00545-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00545-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00545-120">備註</span><span class="sxs-lookup"><span data-stu-id="00545-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="00545-121">需求</span><span class="sxs-lookup"><span data-stu-id="00545-121">Requirements</span></span>



| <span data-ttu-id="00545-122">需求</span><span class="sxs-lookup"><span data-stu-id="00545-122">Requirement</span></span> | <span data-ttu-id="00545-123">值</span><span class="sxs-lookup"><span data-stu-id="00545-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00545-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00545-124">Minimum supported client</span></span><br/> | <span data-ttu-id="00545-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00545-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="00545-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00545-126">Minimum supported server</span></span><br/> | <span data-ttu-id="00545-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00545-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="00545-128">DLL</span><span class="sxs-lookup"><span data-stu-id="00545-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00545-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00545-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




