---
description: 取得裝置的自訂點陣圖標誌。
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'IWiaUIExtension：： GetDeviceBitmapLogo 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972866"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="b525f-103">IWiaUIExtension：： GetDeviceBitmapLogo 方法</span><span class="sxs-lookup"><span data-stu-id="b525f-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="b525f-104">取得裝置的自訂點陣圖標誌。</span><span class="sxs-lookup"><span data-stu-id="b525f-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b525f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b525f-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="b525f-106">參數</span><span class="sxs-lookup"><span data-stu-id="b525f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b525f-107">*bstrDeviceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b525f-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b525f-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b525f-108">Type: **BSTR**</span></span>

<span data-ttu-id="b525f-109">指定要取得其圖示之 WIA 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b525f-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="b525f-110">*phBitmap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b525f-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b525f-111">類型： \**HBITMAP \** _</span><span class="sxs-lookup"><span data-stu-id="b525f-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="b525f-112">指向將接收裝置點陣圖標誌之控制碼的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="b525f-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="b525f-113">_nMaxWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b525f-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b525f-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="b525f-114">Type: **ULONG**</span></span>

<span data-ttu-id="b525f-115">指定點陣圖所需的寬度。</span><span class="sxs-lookup"><span data-stu-id="b525f-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b525f-116">*nMaxHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b525f-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b525f-117">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="b525f-117">Type: **ULONG**</span></span>

<span data-ttu-id="b525f-118">指定所需的點陣圖高度。</span><span class="sxs-lookup"><span data-stu-id="b525f-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b525f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b525f-119">Return value</span></span>

<span data-ttu-id="b525f-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b525f-120">Type: **HRESULT**</span></span>

<span data-ttu-id="b525f-121">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b525f-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b525f-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b525f-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b525f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b525f-123">Requirements</span></span>



| <span data-ttu-id="b525f-124">需求</span><span class="sxs-lookup"><span data-stu-id="b525f-124">Requirement</span></span> | <span data-ttu-id="b525f-125">值</span><span class="sxs-lookup"><span data-stu-id="b525f-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b525f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b525f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b525f-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b525f-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b525f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b525f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b525f-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b525f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b525f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b525f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b525f-131"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="b525f-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




