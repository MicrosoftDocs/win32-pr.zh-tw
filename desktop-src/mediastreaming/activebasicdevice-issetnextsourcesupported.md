---
title: 'ActiveBasicDevice IsSetNextSourceSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出是否支援設定下一個來源。
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- IsSetNextSourceSupported 屬性媒體串流 API
- IsSetNextSourceSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsSetNextSourceSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995584"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="af32b-106">ActiveBasicDevice：： IsSetNextSourceSupported 屬性</span><span class="sxs-lookup"><span data-stu-id="af32b-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="af32b-107">取得值，這個值會指出是否支援設定下一個來源。</span><span class="sxs-lookup"><span data-stu-id="af32b-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="af32b-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="af32b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="af32b-109">語法</span><span class="sxs-lookup"><span data-stu-id="af32b-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="af32b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="af32b-110">Property value</span></span>

<span data-ttu-id="af32b-111">指出是否支援設定下一個來源的 **布林值** 指標。</span><span class="sxs-lookup"><span data-stu-id="af32b-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="af32b-112">如果支援設定下一個來源，則為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="af32b-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="af32b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="af32b-113">Requirements</span></span>



| <span data-ttu-id="af32b-114">需求</span><span class="sxs-lookup"><span data-stu-id="af32b-114">Requirement</span></span> | <span data-ttu-id="af32b-115">值</span><span class="sxs-lookup"><span data-stu-id="af32b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="af32b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af32b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="af32b-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af32b-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="af32b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af32b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="af32b-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af32b-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="af32b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="af32b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="af32b-121"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="af32b-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="af32b-122">Idl</span><span class="sxs-lookup"><span data-stu-id="af32b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af32b-123"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="af32b-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="af32b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="af32b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af32b-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af32b-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af32b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af32b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="af32b-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="af32b-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

