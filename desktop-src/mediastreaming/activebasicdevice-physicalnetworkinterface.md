---
title: 'ActiveBasicDevice PhysicalNetworkInterface 屬性 (PlayToDevice .h) '
description: 取得實體網路介面的識別碼。
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- PhysicalNetworkInterface 屬性媒體串流 API
- PhysicalNetworkInterface 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，PhysicalNetworkInterface 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465741"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="ff4a9-106">ActiveBasicDevice：:P hysicalNetworkInterface 屬性</span><span class="sxs-lookup"><span data-stu-id="ff4a9-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="ff4a9-107">取得實體網路介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff4a9-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="ff4a9-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ff4a9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4a9-109">語法</span><span class="sxs-lookup"><span data-stu-id="ff4a9-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="ff4a9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ff4a9-110">Property value</span></span>

<span data-ttu-id="ff4a9-111">**GUID** 的指標，可指定實體網路介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff4a9-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4a9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff4a9-112">Requirements</span></span>



| <span data-ttu-id="ff4a9-113">需求</span><span class="sxs-lookup"><span data-stu-id="ff4a9-113">Requirement</span></span> | <span data-ttu-id="ff4a9-114">值</span><span class="sxs-lookup"><span data-stu-id="ff4a9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4a9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff4a9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4a9-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff4a9-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff4a9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff4a9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4a9-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff4a9-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ff4a9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ff4a9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff4a9-120"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff4a9-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff4a9-121">Idl</span><span class="sxs-lookup"><span data-stu-id="ff4a9-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff4a9-122"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff4a9-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff4a9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ff4a9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff4a9-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff4a9-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff4a9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff4a9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff4a9-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff4a9-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

