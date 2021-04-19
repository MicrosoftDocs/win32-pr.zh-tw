---
description: 從 Microsoft 媒體基礎影片轉譯接收器取得 IMFDXGIDeviceManager。
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: IMFDXGIDeviceManagerSource：： GetManager 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974641"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="99286-103">IMFDXGIDeviceManagerSource：： GetManager 方法</span><span class="sxs-lookup"><span data-stu-id="99286-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="99286-104">從 Microsoft 媒體基礎影片轉譯接收器取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 。</span><span class="sxs-lookup"><span data-stu-id="99286-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="99286-105">語法</span><span class="sxs-lookup"><span data-stu-id="99286-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="99286-106">參數</span><span class="sxs-lookup"><span data-stu-id="99286-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99286-107">*ppManager* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99286-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99286-108">[**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)物件。</span><span class="sxs-lookup"><span data-stu-id="99286-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99286-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="99286-109">Return value</span></span>

<span data-ttu-id="99286-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="99286-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99286-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99286-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="99286-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="99286-112">Requirements</span></span>



| <span data-ttu-id="99286-113">需求</span><span class="sxs-lookup"><span data-stu-id="99286-113">Requirement</span></span> | <span data-ttu-id="99286-114">值</span><span class="sxs-lookup"><span data-stu-id="99286-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99286-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99286-115">Minimum supported client</span></span><br/> | <span data-ttu-id="99286-116">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99286-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="99286-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99286-117">Minimum supported server</span></span><br/> | <span data-ttu-id="99286-118">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99286-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="99286-119">Idl</span><span class="sxs-lookup"><span data-stu-id="99286-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99286-120"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="99286-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99286-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99286-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99286-122">**IMFDXGIDeviceManagerSource**</span><span class="sxs-lookup"><span data-stu-id="99286-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




