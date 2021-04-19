---
title: 'ActiveBasicDevice GetCachedSinkProtocolInfo 方法 (PlayToDevice .h) '
description: '取得裝置的快取接收通訊協定資訊。 |ActiveBasicDevice GetCachedSinkProtocolInfo 方法 (PlayToDevice .h) '
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- GetCachedSinkProtocolInfo 方法媒體串流 API
- GetCachedSinkProtocolInfo 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetCachedSinkProtocolInfo 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974809"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="4ee91-107">ActiveBasicDevice：： GetCachedSinkProtocolInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4ee91-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="4ee91-108">取得裝置的快取接收通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="4ee91-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee91-109">語法</span><span class="sxs-lookup"><span data-stu-id="4ee91-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="4ee91-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ee91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee91-111">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4ee91-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee91-112">裝置的快取接收通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="4ee91-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee91-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ee91-113">Return value</span></span>

<span data-ttu-id="4ee91-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4ee91-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ee91-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4ee91-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee91-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ee91-116">Requirements</span></span>



| <span data-ttu-id="4ee91-117">需求</span><span class="sxs-lookup"><span data-stu-id="4ee91-117">Requirement</span></span> | <span data-ttu-id="4ee91-118">值</span><span class="sxs-lookup"><span data-stu-id="4ee91-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee91-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ee91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee91-120">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee91-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ee91-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ee91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee91-122">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee91-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ee91-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4ee91-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ee91-124"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ee91-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ee91-125">Idl</span><span class="sxs-lookup"><span data-stu-id="4ee91-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ee91-126"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ee91-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="4ee91-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4ee91-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ee91-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee91-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee91-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ee91-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ee91-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ee91-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

