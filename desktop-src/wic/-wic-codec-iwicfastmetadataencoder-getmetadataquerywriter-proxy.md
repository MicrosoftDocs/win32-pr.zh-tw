---
description: GetMetadataQueryWriter 方法的 IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy 函數 Proxy 函式。
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097166"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="213a9-103">IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="213a9-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="213a9-104">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="213a9-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="213a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="213a9-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="213a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="213a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="213a9-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="213a9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="213a9-108">類型： **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="213a9-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="213a9-109">這個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="213a9-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="213a9-110">*ppIMetadataQueryWriter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="213a9-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="213a9-111">類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="213a9-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="213a9-112">接收編碼器中繼資料查詢寫入器之指標的指標。</span><span class="sxs-lookup"><span data-stu-id="213a9-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="213a9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="213a9-113">Return value</span></span>

<span data-ttu-id="213a9-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="213a9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="213a9-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="213a9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="213a9-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="213a9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="213a9-117">備註</span><span class="sxs-lookup"><span data-stu-id="213a9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="213a9-118">需求</span><span class="sxs-lookup"><span data-stu-id="213a9-118">Requirements</span></span>



| <span data-ttu-id="213a9-119">需求</span><span class="sxs-lookup"><span data-stu-id="213a9-119">Requirement</span></span> | <span data-ttu-id="213a9-120">值</span><span class="sxs-lookup"><span data-stu-id="213a9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="213a9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="213a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="213a9-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="213a9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="213a9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="213a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="213a9-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="213a9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="213a9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="213a9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="213a9-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="213a9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




