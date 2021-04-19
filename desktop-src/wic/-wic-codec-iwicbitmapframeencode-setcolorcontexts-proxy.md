---
description: SetColorCoNtexts 方法的 Proxy 函式。
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: IWICBitmapFrameEncode_SetColorCoNtexts_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8a960873340c15772113a3f1553a9b6e16c44338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973631"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a><span data-ttu-id="759e6-103">IWICBitmapFrameEncode \_ SetColorCoNtexts \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="759e6-103">IWICBitmapFrameEncode\_SetColorContexts\_Proxy function</span></span>

<span data-ttu-id="759e6-104">[**SetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="759e6-104">Proxy function for the [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="759e6-105">語法</span><span class="sxs-lookup"><span data-stu-id="759e6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="759e6-106">參數</span><span class="sxs-lookup"><span data-stu-id="759e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="759e6-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="759e6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759e6-108">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="759e6-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="759e6-109">這個 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="759e6-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="759e6-110">*帳戶 c)* \[在\]</span><span class="sxs-lookup"><span data-stu-id="759e6-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759e6-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="759e6-111">Type: **UINT**</span></span>

<span data-ttu-id="759e6-112">要設定的 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 設定檔數目。</span><span class="sxs-lookup"><span data-stu-id="759e6-112">The number of [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) profiles to set.</span></span>

</dd> <dt>

<span data-ttu-id="759e6-113">*ppIColorCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="759e6-113">*ppIColorContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759e6-114">類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="759e6-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="759e6-115">指向 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 指標的指標，其中包含要設定至框架的色彩內容設定檔。</span><span class="sxs-lookup"><span data-stu-id="759e6-115">A pointer to an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pointer containing the color contexts profiles to set to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="759e6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="759e6-116">Return value</span></span>

<span data-ttu-id="759e6-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="759e6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="759e6-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="759e6-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="759e6-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="759e6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="759e6-120">備註</span><span class="sxs-lookup"><span data-stu-id="759e6-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="759e6-121">需求</span><span class="sxs-lookup"><span data-stu-id="759e6-121">Requirements</span></span>



| <span data-ttu-id="759e6-122">需求</span><span class="sxs-lookup"><span data-stu-id="759e6-122">Requirement</span></span> | <span data-ttu-id="759e6-123">值</span><span class="sxs-lookup"><span data-stu-id="759e6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="759e6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="759e6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="759e6-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="759e6-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="759e6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="759e6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="759e6-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="759e6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="759e6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="759e6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="759e6-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="759e6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




