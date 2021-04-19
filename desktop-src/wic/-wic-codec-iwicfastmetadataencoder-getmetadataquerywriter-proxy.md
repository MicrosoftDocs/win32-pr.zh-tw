---
description: GetMetadataQueryWriter 方法的 Proxy 函式。
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
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980491"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="585d2-103">IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="585d2-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="585d2-104">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="585d2-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="585d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="585d2-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="585d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="585d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585d2-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="585d2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="585d2-108">類型： \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="585d2-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="585d2-109">這個 [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="585d2-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="585d2-110">*ppIMetadataQueryWriter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="585d2-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="585d2-111">類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="585d2-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="585d2-112">接收編碼器中繼資料查詢寫入器之指標的指標。</span><span class="sxs-lookup"><span data-stu-id="585d2-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="585d2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="585d2-113">Return value</span></span>

<span data-ttu-id="585d2-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="585d2-114">Type: **HRESULT**</span></span>

<span data-ttu-id="585d2-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="585d2-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="585d2-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="585d2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="585d2-117">備註</span><span class="sxs-lookup"><span data-stu-id="585d2-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="585d2-118">需求</span><span class="sxs-lookup"><span data-stu-id="585d2-118">Requirements</span></span>



| <span data-ttu-id="585d2-119">需求</span><span class="sxs-lookup"><span data-stu-id="585d2-119">Requirement</span></span> | <span data-ttu-id="585d2-120">值</span><span class="sxs-lookup"><span data-stu-id="585d2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="585d2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="585d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="585d2-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="585d2-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="585d2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="585d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="585d2-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="585d2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="585d2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="585d2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="585d2-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="585d2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




