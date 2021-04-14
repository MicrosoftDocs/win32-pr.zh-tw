---
description: Commit 方法的 Proxy 函數。
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318259"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="57cc7-103">IWICBitmapFrameEncode \_ Commit \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="57cc7-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="57cc7-104">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)方法的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="57cc7-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57cc7-105">語法</span><span class="sxs-lookup"><span data-stu-id="57cc7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="57cc7-106">參數</span><span class="sxs-lookup"><span data-stu-id="57cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cc7-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="57cc7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cc7-108">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="57cc7-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="57cc7-109">這個 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="57cc7-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cc7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="57cc7-110">Return value</span></span>

<span data-ttu-id="57cc7-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="57cc7-111">Type: **HRESULT**</span></span>

<span data-ttu-id="57cc7-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="57cc7-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57cc7-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57cc7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57cc7-114">備註</span><span class="sxs-lookup"><span data-stu-id="57cc7-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="57cc7-115">需求</span><span class="sxs-lookup"><span data-stu-id="57cc7-115">Requirements</span></span>



| <span data-ttu-id="57cc7-116">需求</span><span class="sxs-lookup"><span data-stu-id="57cc7-116">Requirement</span></span> | <span data-ttu-id="57cc7-117">值</span><span class="sxs-lookup"><span data-stu-id="57cc7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57cc7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57cc7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57cc7-119">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57cc7-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="57cc7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57cc7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57cc7-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57cc7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="57cc7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="57cc7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57cc7-123"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57cc7-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




