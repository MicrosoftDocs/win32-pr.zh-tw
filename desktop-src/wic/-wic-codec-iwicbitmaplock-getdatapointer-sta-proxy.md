---
description: GetDataPointer 方法的 Proxy 函式。
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997252"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="27479-103">IWICBitmapLock \_ GetDataPointer \_ STA \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="27479-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="27479-104">[**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="27479-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27479-105">語法</span><span class="sxs-lookup"><span data-stu-id="27479-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="27479-106">參數</span><span class="sxs-lookup"><span data-stu-id="27479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27479-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="27479-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27479-108">類型： \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="27479-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="27479-109">這個 [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="27479-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="27479-110">*pcbBufferSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="27479-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27479-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="27479-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="27479-112">接收緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="27479-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="27479-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27479-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27479-114">類型：**位元組 \* \***</span><span class="sxs-lookup"><span data-stu-id="27479-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="27479-115">指標，可接收鎖定矩形中左上角圖元的指標。</span><span class="sxs-lookup"><span data-stu-id="27479-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27479-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="27479-116">Return value</span></span>

<span data-ttu-id="27479-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27479-117">Type: **HRESULT**</span></span>

<span data-ttu-id="27479-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="27479-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27479-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="27479-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27479-120">備註</span><span class="sxs-lookup"><span data-stu-id="27479-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="27479-121">需求</span><span class="sxs-lookup"><span data-stu-id="27479-121">Requirements</span></span>



| <span data-ttu-id="27479-122">需求</span><span class="sxs-lookup"><span data-stu-id="27479-122">Requirement</span></span> | <span data-ttu-id="27479-123">值</span><span class="sxs-lookup"><span data-stu-id="27479-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27479-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27479-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27479-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27479-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="27479-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27479-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27479-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27479-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="27479-128">DLL</span><span class="sxs-lookup"><span data-stu-id="27479-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27479-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="27479-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




