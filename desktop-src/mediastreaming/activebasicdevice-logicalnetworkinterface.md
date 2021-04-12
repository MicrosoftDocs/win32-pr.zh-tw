---
title: 'ActiveBasicDevice LogicalNetworkInterface 屬性 (PlayToDevice .h) '
description: 取得邏輯網路介面的識別碼。
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- LogicalNetworkInterface 屬性媒體串流 API
- LogicalNetworkInterface 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，LogicalNetworkInterface 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384509"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="32de6-106">ActiveBasicDevice：： LogicalNetworkInterface 屬性</span><span class="sxs-lookup"><span data-stu-id="32de6-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="32de6-107">取得邏輯網路介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="32de6-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="32de6-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="32de6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32de6-109">語法</span><span class="sxs-lookup"><span data-stu-id="32de6-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="32de6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="32de6-110">Property value</span></span>

<span data-ttu-id="32de6-111">**GUID** 的指標，指定邏輯網路介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="32de6-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="32de6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="32de6-112">Requirements</span></span>



| <span data-ttu-id="32de6-113">需求</span><span class="sxs-lookup"><span data-stu-id="32de6-113">Requirement</span></span> | <span data-ttu-id="32de6-114">值</span><span class="sxs-lookup"><span data-stu-id="32de6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="32de6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32de6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="32de6-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32de6-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="32de6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32de6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="32de6-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32de6-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="32de6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="32de6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="32de6-120"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="32de6-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="32de6-121">Idl</span><span class="sxs-lookup"><span data-stu-id="32de6-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32de6-122"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="32de6-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="32de6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="32de6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32de6-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32de6-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32de6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32de6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="32de6-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32de6-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

