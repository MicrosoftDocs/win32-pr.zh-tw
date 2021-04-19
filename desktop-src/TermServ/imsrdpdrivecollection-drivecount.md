---
title: IMsRdpDriveCollection DriveCount 屬性
description: 抓取集合中的物件計數。 |IMsRdpDriveCollection DriveCount 屬性
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- DriveCount 屬性遠端桌面服務
- DriveCount 屬性遠端桌面服務，IMsRdpDriveCollection 介面
- IMsRdpDriveCollection 介面遠端桌面服務，DriveCount 屬性
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991433"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="68f6b-107">IMsRdpDriveCollection：:D riveCount 屬性</span><span class="sxs-lookup"><span data-stu-id="68f6b-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="68f6b-108">抓取集合中的物件計數。</span><span class="sxs-lookup"><span data-stu-id="68f6b-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="68f6b-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="68f6b-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f6b-110">語法</span><span class="sxs-lookup"><span data-stu-id="68f6b-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="68f6b-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="68f6b-111">Property value</span></span>

<span data-ttu-id="68f6b-112">物件計數。</span><span class="sxs-lookup"><span data-stu-id="68f6b-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68f6b-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="68f6b-113">Error codes</span></span>

<span data-ttu-id="68f6b-114">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="68f6b-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="68f6b-115">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="68f6b-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f6b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="68f6b-116">Requirements</span></span>



| <span data-ttu-id="68f6b-117">需求</span><span class="sxs-lookup"><span data-stu-id="68f6b-117">Requirement</span></span> | <span data-ttu-id="68f6b-118">值</span><span class="sxs-lookup"><span data-stu-id="68f6b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f6b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68f6b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68f6b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68f6b-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="68f6b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68f6b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68f6b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68f6b-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="68f6b-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="68f6b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="68f6b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f6b-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="68f6b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="68f6b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68f6b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f6b-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="68f6b-127">IID</span><span class="sxs-lookup"><span data-stu-id="68f6b-127">IID</span></span><br/>                      | <span data-ttu-id="68f6b-128">IID \_ IMsRdpDriveCollection 定義為 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="68f6b-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68f6b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68f6b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f6b-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="68f6b-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





