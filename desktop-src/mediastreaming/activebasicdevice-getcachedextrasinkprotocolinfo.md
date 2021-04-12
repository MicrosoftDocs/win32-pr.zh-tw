---
title: 'ActiveBasicDevice GetCachedExtraSinkProtocolInfo 方法 (PlayToDevice .h) '
description: 取得裝置的其他快取接收通訊協定資訊。
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- GetCachedExtraSinkProtocolInfo 方法媒體串流 API
- GetCachedExtraSinkProtocolInfo 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetCachedExtraSinkProtocolInfo 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384850"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="a06e1-106">ActiveBasicDevice：： GetCachedExtraSinkProtocolInfo 方法</span><span class="sxs-lookup"><span data-stu-id="a06e1-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="a06e1-107">取得裝置的其他快取接收通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="a06e1-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a06e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="a06e1-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="a06e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="a06e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a06e1-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a06e1-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a06e1-111">裝置的額外快取接收通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="a06e1-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a06e1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a06e1-112">Return value</span></span>

<span data-ttu-id="a06e1-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a06e1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a06e1-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a06e1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a06e1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a06e1-115">Requirements</span></span>



| <span data-ttu-id="a06e1-116">需求</span><span class="sxs-lookup"><span data-stu-id="a06e1-116">Requirement</span></span> | <span data-ttu-id="a06e1-117">值</span><span class="sxs-lookup"><span data-stu-id="a06e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a06e1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a06e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a06e1-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a06e1-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a06e1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a06e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a06e1-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a06e1-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a06e1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a06e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a06e1-123"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="a06e1-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="a06e1-124">Idl</span><span class="sxs-lookup"><span data-stu-id="a06e1-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a06e1-125"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a06e1-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="a06e1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a06e1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a06e1-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a06e1-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a06e1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a06e1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a06e1-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a06e1-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

