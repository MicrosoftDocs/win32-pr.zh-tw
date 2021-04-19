---
description: GetLocation 方法的 Proxy 函式。
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: IWICMetadataQueryReader_GetLocation_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985702"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="16e30-103">IWICMetadataQueryReader \_ GetLocation \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="16e30-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="16e30-104">[**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="16e30-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e30-105">語法</span><span class="sxs-lookup"><span data-stu-id="16e30-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="16e30-106">參數</span><span class="sxs-lookup"><span data-stu-id="16e30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e30-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="16e30-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e30-108">類型： \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="16e30-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="16e30-109">這個 [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="16e30-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="16e30-110">*cchMaxLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16e30-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e30-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="16e30-111">Type: **UINT**</span></span>

<span data-ttu-id="16e30-112">*WzNamespace* 緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="16e30-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="16e30-113">*wzNamespace* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="16e30-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16e30-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="16e30-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="16e30-115">接收目前命名空間位置的指標。</span><span class="sxs-lookup"><span data-stu-id="16e30-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="16e30-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="16e30-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16e30-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="16e30-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="16e30-118">取得目前命名空間位置所需的實際緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="16e30-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e30-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="16e30-119">Return value</span></span>

<span data-ttu-id="16e30-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="16e30-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="16e30-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="16e30-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16e30-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="16e30-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e30-123">備註</span><span class="sxs-lookup"><span data-stu-id="16e30-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="16e30-124">需求</span><span class="sxs-lookup"><span data-stu-id="16e30-124">Requirements</span></span>



| <span data-ttu-id="16e30-125">需求</span><span class="sxs-lookup"><span data-stu-id="16e30-125">Requirement</span></span> | <span data-ttu-id="16e30-126">值</span><span class="sxs-lookup"><span data-stu-id="16e30-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e30-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16e30-127">Minimum supported client</span></span><br/> | <span data-ttu-id="16e30-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16e30-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="16e30-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16e30-129">Minimum supported server</span></span><br/> | <span data-ttu-id="16e30-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16e30-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="16e30-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16e30-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16e30-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16e30-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




