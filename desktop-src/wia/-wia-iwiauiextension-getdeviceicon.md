---
description: 取得自訂裝置圖示。
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension：： GetDeviceIcon 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113292"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="d5308-103">IWiaUIExtension：： GetDeviceIcon 方法</span><span class="sxs-lookup"><span data-stu-id="d5308-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="d5308-104">取得自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="d5308-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5308-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5308-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="d5308-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5308-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5308-107">*bstrDeviceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5308-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5308-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d5308-108">Type: **BSTR**</span></span>

<span data-ttu-id="d5308-109">指定要取得其圖示之 WIA 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5308-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="d5308-110">*phIcon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5308-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5308-111">類型： \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="d5308-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="d5308-112">指向將接收裝置圖示控制碼的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="d5308-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="d5308-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5308-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5308-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="d5308-114">Type: **ULONG**</span></span>

<span data-ttu-id="d5308-115">指定所需的圖示大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5308-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="d5308-116">此圖示會假設為正方形，而 nSize 會指定所要求圖示的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="d5308-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5308-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5308-117">Return value</span></span>

<span data-ttu-id="d5308-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5308-118">Type: **HRESULT**</span></span>

<span data-ttu-id="d5308-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d5308-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5308-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d5308-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5308-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5308-121">Requirements</span></span>



| <span data-ttu-id="d5308-122">需求</span><span class="sxs-lookup"><span data-stu-id="d5308-122">Requirement</span></span> | <span data-ttu-id="d5308-123">值</span><span class="sxs-lookup"><span data-stu-id="d5308-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5308-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5308-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d5308-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5308-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d5308-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5308-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d5308-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5308-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d5308-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d5308-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5308-129"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5308-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




