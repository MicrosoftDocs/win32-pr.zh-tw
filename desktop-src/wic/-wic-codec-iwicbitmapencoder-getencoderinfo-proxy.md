---
description: GetEncoderInfo 方法的 Proxy 函式。
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: IWICBitmapEncoder_GetEncoderInfo_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984261"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="4d780-103">IWICBitmapEncoder \_ GetEncoderInfo \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="4d780-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="4d780-104">[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="4d780-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d780-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d780-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4d780-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d780-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="4d780-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d780-108">類型： \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="4d780-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="4d780-109">這個 [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4d780-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="4d780-110">*ppIEncoderInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d780-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d780-111">類型： **[ **IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="4d780-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="4d780-112">接收 [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="4d780-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d780-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d780-113">Return value</span></span>

<span data-ttu-id="4d780-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4d780-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4d780-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4d780-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d780-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4d780-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d780-117">備註</span><span class="sxs-lookup"><span data-stu-id="4d780-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4d780-118">需求</span><span class="sxs-lookup"><span data-stu-id="4d780-118">Requirements</span></span>



| <span data-ttu-id="4d780-119">需求</span><span class="sxs-lookup"><span data-stu-id="4d780-119">Requirement</span></span> | <span data-ttu-id="4d780-120">值</span><span class="sxs-lookup"><span data-stu-id="4d780-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d780-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d780-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4d780-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d780-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4d780-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d780-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4d780-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d780-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4d780-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4d780-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d780-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




