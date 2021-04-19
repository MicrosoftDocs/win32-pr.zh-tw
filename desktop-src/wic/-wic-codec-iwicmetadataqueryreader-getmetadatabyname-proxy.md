---
description: GetMetadataByName 方法的 Proxy 函式。
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000159"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="54a90-103">IWICMetadataQueryReader \_ GetMetadataByName \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="54a90-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="54a90-104">[**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="54a90-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a90-105">語法</span><span class="sxs-lookup"><span data-stu-id="54a90-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="54a90-106">參數</span><span class="sxs-lookup"><span data-stu-id="54a90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a90-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="54a90-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a90-108">類型： \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="54a90-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="54a90-109">這個 [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="54a90-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="54a90-110">*wzName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54a90-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a90-111">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="54a90-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="54a90-112">要求的中繼資料專案名稱。</span><span class="sxs-lookup"><span data-stu-id="54a90-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="54a90-113">*pvarValue* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="54a90-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54a90-114">類型： \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="54a90-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="54a90-115">接收中繼資料屬性的指標。</span><span class="sxs-lookup"><span data-stu-id="54a90-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a90-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="54a90-116">Return value</span></span>

<span data-ttu-id="54a90-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="54a90-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="54a90-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="54a90-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54a90-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="54a90-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a90-120">備註</span><span class="sxs-lookup"><span data-stu-id="54a90-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="54a90-121">需求</span><span class="sxs-lookup"><span data-stu-id="54a90-121">Requirements</span></span>



| <span data-ttu-id="54a90-122">需求</span><span class="sxs-lookup"><span data-stu-id="54a90-122">Requirement</span></span> | <span data-ttu-id="54a90-123">值</span><span class="sxs-lookup"><span data-stu-id="54a90-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a90-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54a90-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54a90-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54a90-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="54a90-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54a90-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54a90-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54a90-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="54a90-128">DLL</span><span class="sxs-lookup"><span data-stu-id="54a90-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54a90-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="54a90-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

