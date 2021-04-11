---
description: InitializeFromIStream 方法的 Proxy 函式。
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194130"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a><span data-ttu-id="f3cac-103">IWICStream \_ InitializeFromIStream \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="f3cac-103">IWICStream\_InitializeFromIStream\_Proxy function</span></span>

<span data-ttu-id="f3cac-104">[**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="f3cac-104">Proxy function for the [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3cac-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3cac-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a><span data-ttu-id="f3cac-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3cac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3cac-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="f3cac-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cac-108">類型： \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="f3cac-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="f3cac-109">這個 [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f3cac-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="f3cac-110">*pIStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3cac-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cac-111">類型： \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="f3cac-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="f3cac-112">Initialize 資料流程。</span><span class="sxs-lookup"><span data-stu-id="f3cac-112">The initialize stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3cac-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3cac-113">Return value</span></span>

<span data-ttu-id="f3cac-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f3cac-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f3cac-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f3cac-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3cac-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3cac-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3cac-117">備註</span><span class="sxs-lookup"><span data-stu-id="f3cac-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f3cac-118">需求</span><span class="sxs-lookup"><span data-stu-id="f3cac-118">Requirements</span></span>



| <span data-ttu-id="f3cac-119">需求</span><span class="sxs-lookup"><span data-stu-id="f3cac-119">Requirement</span></span> | <span data-ttu-id="f3cac-120">值</span><span class="sxs-lookup"><span data-stu-id="f3cac-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cac-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3cac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f3cac-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3cac-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f3cac-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3cac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f3cac-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3cac-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f3cac-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f3cac-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3cac-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3cac-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

