---
description: GetEnumerator 方法的 Proxy 函式。
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: IWICMetadataQueryReader_GetEnumerator_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992085"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="1671d-103">IWICMetadataQueryReader \_ GetEnumerator \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="1671d-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="1671d-104">[**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="1671d-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1671d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1671d-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="1671d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1671d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1671d-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="1671d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1671d-108">類型： \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="1671d-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="1671d-109">這個 [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="1671d-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="1671d-110">*ppIEnumString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1671d-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1671d-111">類型： **IEnumString \* \***</span><span class="sxs-lookup"><span data-stu-id="1671d-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="1671d-112">接收中繼資料列舉值指標的指標。</span><span class="sxs-lookup"><span data-stu-id="1671d-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1671d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1671d-113">Return value</span></span>

<span data-ttu-id="1671d-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1671d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1671d-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1671d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1671d-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1671d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1671d-117">備註</span><span class="sxs-lookup"><span data-stu-id="1671d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1671d-118">需求</span><span class="sxs-lookup"><span data-stu-id="1671d-118">Requirements</span></span>



| <span data-ttu-id="1671d-119">需求</span><span class="sxs-lookup"><span data-stu-id="1671d-119">Requirement</span></span> | <span data-ttu-id="1671d-120">值</span><span class="sxs-lookup"><span data-stu-id="1671d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1671d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1671d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1671d-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1671d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1671d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1671d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1671d-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1671d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1671d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1671d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1671d-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1671d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




