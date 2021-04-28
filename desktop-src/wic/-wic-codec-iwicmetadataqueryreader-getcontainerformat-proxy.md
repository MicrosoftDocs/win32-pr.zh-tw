---
description: GetContainerFormat 方法的 IWICMetadataQueryReader_GetContainerFormat_Proxy 函數 Proxy 函式。
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097136"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="a0c6c-103">IWICMetadataQueryReader \_ GetContainerFormat \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="a0c6c-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="a0c6c-104">[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="a0c6c-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0c6c-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a0c6c-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0c6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0c6c-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="a0c6c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0c6c-108">類型： **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="a0c6c-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="a0c6c-109">這個 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a0c6c-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="a0c6c-110">*pguidContainerFormat* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a0c6c-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0c6c-111">類型： **GUID \***</span><span class="sxs-lookup"><span data-stu-id="a0c6c-111">Type: **GUID\***</span></span>

<span data-ttu-id="a0c6c-112">接收 cointainer 格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="a0c6c-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0c6c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0c6c-113">Return value</span></span>

<span data-ttu-id="a0c6c-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a0c6c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a0c6c-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a0c6c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0c6c-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a0c6c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0c6c-117">備註</span><span class="sxs-lookup"><span data-stu-id="a0c6c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a0c6c-118">需求</span><span class="sxs-lookup"><span data-stu-id="a0c6c-118">Requirements</span></span>



| <span data-ttu-id="a0c6c-119">需求</span><span class="sxs-lookup"><span data-stu-id="a0c6c-119">Requirement</span></span> | <span data-ttu-id="a0c6c-120">值</span><span class="sxs-lookup"><span data-stu-id="a0c6c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c6c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0c6c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0c6c-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0c6c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a0c6c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0c6c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0c6c-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0c6c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a0c6c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a0c6c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0c6c-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0c6c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




