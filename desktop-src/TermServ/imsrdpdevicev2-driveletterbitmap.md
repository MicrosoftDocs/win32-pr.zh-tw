---
title: IMsRdpDeviceV2 DriveLetterBitmap 屬性
description: 包含代表裝置內所含之磁碟機號對應的位位。
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- DriveLetterBitmap 屬性遠端桌面服務
- DriveLetterBitmap 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，DriveLetterBitmap 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685531"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="03279-106">IMsRdpDeviceV2：:D riveLetterBitmap 屬性</span><span class="sxs-lookup"><span data-stu-id="03279-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="03279-107">包含代表裝置內所含之磁碟機號對應的位位。</span><span class="sxs-lookup"><span data-stu-id="03279-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="03279-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="03279-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03279-109">語法</span><span class="sxs-lookup"><span data-stu-id="03279-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="03279-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="03279-110">Property value</span></span>

<span data-ttu-id="03279-111">包含在裝置內的磁碟機號對應。</span><span class="sxs-lookup"><span data-stu-id="03279-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="03279-112">值中的每個位都代表一個磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="03279-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="03279-113">最不重要的位代表磁碟機號 "A"，下一個位代表磁碟機號 "B"，依此類推。</span><span class="sxs-lookup"><span data-stu-id="03279-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="03279-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="03279-114">Requirements</span></span>



| <span data-ttu-id="03279-115">需求</span><span class="sxs-lookup"><span data-stu-id="03279-115">Requirement</span></span> | <span data-ttu-id="03279-116">值</span><span class="sxs-lookup"><span data-stu-id="03279-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03279-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03279-117">Minimum supported client</span></span><br/> | <span data-ttu-id="03279-118">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="03279-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="03279-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03279-119">Minimum supported server</span></span><br/> | <span data-ttu-id="03279-120">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="03279-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="03279-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="03279-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="03279-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03279-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="03279-123">DLL</span><span class="sxs-lookup"><span data-stu-id="03279-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03279-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03279-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="03279-125">IID</span><span class="sxs-lookup"><span data-stu-id="03279-125">IID</span></span><br/>                      | <span data-ttu-id="03279-126">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="03279-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="03279-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03279-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03279-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="03279-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





