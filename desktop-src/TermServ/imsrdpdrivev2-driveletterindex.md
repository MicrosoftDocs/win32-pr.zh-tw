---
title: IMsRdpDriveV2 DriveLetterIndex 屬性
description: 包含磁片磁碟機的字母索引。
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- DriveLetterIndex 屬性遠端桌面服務
- DriveLetterIndex 屬性遠端桌面服務，IMsRdpDriveV2 介面
- IMsRdpDriveV2 介面遠端桌面服務，DriveLetterIndex 屬性
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935130"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="92113-106">IMsRdpDriveV2：:D riveLetterIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="92113-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="92113-107">包含磁片磁碟機的字母索引。</span><span class="sxs-lookup"><span data-stu-id="92113-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="92113-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="92113-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92113-109">語法</span><span class="sxs-lookup"><span data-stu-id="92113-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="92113-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="92113-110">Property value</span></span>

<span data-ttu-id="92113-111">磁片磁碟機的字母索引。</span><span class="sxs-lookup"><span data-stu-id="92113-111">The index of the letter for the drive.</span></span> <span data-ttu-id="92113-112">0 = "A"、1 = "B" 等等。</span><span class="sxs-lookup"><span data-stu-id="92113-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="92113-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="92113-113">Requirements</span></span>



| <span data-ttu-id="92113-114">需求</span><span class="sxs-lookup"><span data-stu-id="92113-114">Requirement</span></span> | <span data-ttu-id="92113-115">值</span><span class="sxs-lookup"><span data-stu-id="92113-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92113-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92113-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92113-117">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="92113-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="92113-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92113-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92113-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92113-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="92113-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="92113-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="92113-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92113-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="92113-122">DLL</span><span class="sxs-lookup"><span data-stu-id="92113-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92113-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92113-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92113-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92113-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92113-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="92113-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





