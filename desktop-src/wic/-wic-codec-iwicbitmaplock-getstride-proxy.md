---
description: GetStride 方法的 Proxy 函式。
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: IWICBitmapLock_GetStride_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989978"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="6fb8b-103">IWICBitmapLock \_ GetStride \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="6fb8b-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="6fb8b-104">[**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="6fb8b-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb8b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6fb8b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="6fb8b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6fb8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fb8b-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="6fb8b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb8b-108">類型： \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="6fb8b-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="6fb8b-109">這個 [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6fb8b-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8b-110">*pcbStride* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6fb8b-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb8b-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="6fb8b-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="6fb8b-112">點陣圖跨距。</span><span class="sxs-lookup"><span data-stu-id="6fb8b-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fb8b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6fb8b-113">Return value</span></span>

<span data-ttu-id="6fb8b-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6fb8b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6fb8b-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6fb8b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fb8b-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6fb8b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb8b-117">備註</span><span class="sxs-lookup"><span data-stu-id="6fb8b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb8b-118">需求</span><span class="sxs-lookup"><span data-stu-id="6fb8b-118">Requirements</span></span>



| <span data-ttu-id="6fb8b-119">需求</span><span class="sxs-lookup"><span data-stu-id="6fb8b-119">Requirement</span></span> | <span data-ttu-id="6fb8b-120">值</span><span class="sxs-lookup"><span data-stu-id="6fb8b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb8b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fb8b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb8b-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb8b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6fb8b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fb8b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb8b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb8b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6fb8b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb8b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fb8b-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fb8b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




