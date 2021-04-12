---
title: IMsRdpDriveCollection DriveByIndex 屬性
description: 抓取位於指定之索引處的磁片磁碟機。
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- DriveByIndex 屬性遠端桌面服務
- DriveByIndex 屬性遠端桌面服務，IMsRdpDriveCollection 介面
- IMsRdpDriveCollection 介面遠端桌面服務，DriveByIndex 屬性
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384982"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="05e4e-106">IMsRdpDriveCollection：:D riveByIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="05e4e-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="05e4e-107">抓取位於指定之索引處的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05e4e-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="05e4e-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="05e4e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e4e-109">語法</span><span class="sxs-lookup"><span data-stu-id="05e4e-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="05e4e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="05e4e-110">Property value</span></span>

<span data-ttu-id="05e4e-111">[**IMsRdpDrive**](imsrdpdrive.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="05e4e-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05e4e-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="05e4e-112">Error codes</span></span>

<span data-ttu-id="05e4e-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="05e4e-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="05e4e-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="05e4e-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e4e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="05e4e-115">Requirements</span></span>



| <span data-ttu-id="05e4e-116">需求</span><span class="sxs-lookup"><span data-stu-id="05e4e-116">Requirement</span></span> | <span data-ttu-id="05e4e-117">值</span><span class="sxs-lookup"><span data-stu-id="05e4e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05e4e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05e4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05e4e-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05e4e-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="05e4e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05e4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05e4e-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05e4e-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="05e4e-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="05e4e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="05e4e-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05e4e-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="05e4e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="05e4e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05e4e-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05e4e-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="05e4e-126">IID</span><span class="sxs-lookup"><span data-stu-id="05e4e-126">IID</span></span><br/>                      | <span data-ttu-id="05e4e-127">IID \_ IMsRdpDriveCollection 定義為 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="05e4e-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05e4e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05e4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e4e-129">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="05e4e-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





