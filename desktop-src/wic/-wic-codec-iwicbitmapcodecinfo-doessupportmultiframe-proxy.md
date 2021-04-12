---
description: DoesSupportMultiframe 方法的 Proxy 函式。
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112849"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="15f42-103">IWICBitmapCodecInfo \_ DoesSupportMultiframe \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="15f42-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="15f42-104">[**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="15f42-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f42-105">語法</span><span class="sxs-lookup"><span data-stu-id="15f42-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="15f42-106">參數</span><span class="sxs-lookup"><span data-stu-id="15f42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f42-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="15f42-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15f42-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="15f42-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="15f42-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="15f42-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="15f42-110">*pfSupportMultiframe* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="15f42-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15f42-111">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="15f42-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="15f42-112">如果編解碼器支援多個框架影像，則為接收 _ *TRUE*\* 的指標;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="15f42-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f42-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="15f42-113">Return value</span></span>

<span data-ttu-id="15f42-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15f42-114">Type: **HRESULT**</span></span>

<span data-ttu-id="15f42-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="15f42-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15f42-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="15f42-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f42-117">備註</span><span class="sxs-lookup"><span data-stu-id="15f42-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="15f42-118">需求</span><span class="sxs-lookup"><span data-stu-id="15f42-118">Requirements</span></span>



| <span data-ttu-id="15f42-119">需求</span><span class="sxs-lookup"><span data-stu-id="15f42-119">Requirement</span></span> | <span data-ttu-id="15f42-120">值</span><span class="sxs-lookup"><span data-stu-id="15f42-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f42-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15f42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15f42-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15f42-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="15f42-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15f42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15f42-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15f42-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="15f42-125">DLL</span><span class="sxs-lookup"><span data-stu-id="15f42-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15f42-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="15f42-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




