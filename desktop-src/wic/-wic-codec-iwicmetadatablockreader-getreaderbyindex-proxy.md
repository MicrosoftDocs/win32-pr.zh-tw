---
description: GetReaderByIndex 方法的 Proxy 函式。
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: IWICMetadataBlockReader_GetReaderByIndex_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983853"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a><span data-ttu-id="5c3ca-103">IWICMetadataBlockReader \_ GetReaderByIndex \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="5c3ca-103">IWICMetadataBlockReader\_GetReaderByIndex\_Proxy function</span></span>

<span data-ttu-id="5c3ca-104">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="5c3ca-104">Proxy function for the [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c3ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c3ca-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a><span data-ttu-id="5c3ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c3ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c3ca-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="5c3ca-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3ca-108">類型： \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="5c3ca-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="5c3ca-109">這個 [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="5c3ca-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="5c3ca-110">*nIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c3ca-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3ca-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="5c3ca-111">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="5c3ca-112">*ppIMetadataReader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5c3ca-112">*ppIMetadataReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3ca-113">類型： **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c3ca-113">Type: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c3ca-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c3ca-114">Return value</span></span>

<span data-ttu-id="5c3ca-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c3ca-115">Type: **HRESULT**</span></span>

<span data-ttu-id="5c3ca-116">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5c3ca-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c3ca-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c3ca-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c3ca-118">備註</span><span class="sxs-lookup"><span data-stu-id="5c3ca-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5c3ca-119">需求</span><span class="sxs-lookup"><span data-stu-id="5c3ca-119">Requirements</span></span>



| <span data-ttu-id="5c3ca-120">需求</span><span class="sxs-lookup"><span data-stu-id="5c3ca-120">Requirement</span></span> | <span data-ttu-id="5c3ca-121">值</span><span class="sxs-lookup"><span data-stu-id="5c3ca-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c3ca-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c3ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c3ca-123">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c3ca-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5c3ca-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c3ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c3ca-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c3ca-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5c3ca-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5c3ca-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c3ca-127"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c3ca-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




