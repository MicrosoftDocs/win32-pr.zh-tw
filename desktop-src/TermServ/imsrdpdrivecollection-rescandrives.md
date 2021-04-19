---
title: IMsRdpDriveCollection RescanDrives 方法
description: 重新整理集合中的物件清單。 |IMsRdpDriveCollection RescanDrives 方法
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- RescanDrives 方法遠端桌面服務
- RescanDrives 方法遠端桌面服務，IMsRdpDriveCollection 介面
- IMsRdpDriveCollection 介面遠端桌面服務，RescanDrives 方法
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992669"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="e2f5d-107">IMsRdpDriveCollection：： RescanDrives 方法</span><span class="sxs-lookup"><span data-stu-id="e2f5d-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="e2f5d-108">重新整理集合中的物件清單。</span><span class="sxs-lookup"><span data-stu-id="e2f5d-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f5d-109">語法</span><span class="sxs-lookup"><span data-stu-id="e2f5d-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="e2f5d-110">參數</span><span class="sxs-lookup"><span data-stu-id="e2f5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f5d-111">*vboolDynRedir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2f5d-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f5d-112">預設會套用至任何新探索到的裝置或磁片磁碟機的重新導向狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f5d-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f5d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2f5d-113">Return value</span></span>

<span data-ttu-id="e2f5d-114">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e2f5d-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e2f5d-115">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="e2f5d-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f5d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2f5d-116">Requirements</span></span>



| <span data-ttu-id="e2f5d-117">需求</span><span class="sxs-lookup"><span data-stu-id="e2f5d-117">Requirement</span></span> | <span data-ttu-id="e2f5d-118">值</span><span class="sxs-lookup"><span data-stu-id="e2f5d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f5d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2f5d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f5d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2f5d-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e2f5d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2f5d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f5d-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2f5d-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e2f5d-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e2f5d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2f5d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f5d-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e2f5d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f5d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f5d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f5d-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e2f5d-127">IID</span><span class="sxs-lookup"><span data-stu-id="e2f5d-127">IID</span></span><br/>                      | <span data-ttu-id="e2f5d-128">IID \_ IMsRdpDriveCollection 定義為 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="e2f5d-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2f5d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2f5d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f5d-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="e2f5d-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





