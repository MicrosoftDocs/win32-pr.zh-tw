---
description: 指定影片內容的保護層級。
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: 'D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970353"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="26ed3-103">D3DAUTHENTICATEDCHANNEL \_ 保護 \_ 旗標結構</span><span class="sxs-lookup"><span data-stu-id="26ed3-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="26ed3-104">指定影片內容的保護層級。</span><span class="sxs-lookup"><span data-stu-id="26ed3-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ed3-105">語法</span><span class="sxs-lookup"><span data-stu-id="26ed3-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="26ed3-106">成員</span><span class="sxs-lookup"><span data-stu-id="26ed3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="26ed3-107">**ProtectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="26ed3-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-108">若為1，則會啟用影片內容保護。</span><span class="sxs-lookup"><span data-stu-id="26ed3-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="26ed3-109">**OverlayOrFullscreenRequired**</span><span class="sxs-lookup"><span data-stu-id="26ed3-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-110">如果是1，則應用程式需要使用硬體重迭或全螢幕獨佔模式來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="26ed3-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="26ed3-111">**已保留**</span><span class="sxs-lookup"><span data-stu-id="26ed3-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="26ed3-112">Reserved.</span></span> <span data-ttu-id="26ed3-113">將所有位設為零。</span><span class="sxs-lookup"><span data-stu-id="26ed3-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="26ed3-114">**值**</span><span class="sxs-lookup"><span data-stu-id="26ed3-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="26ed3-115">您可以使用這個成員來存取等位中的所有位。</span><span class="sxs-lookup"><span data-stu-id="26ed3-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26ed3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="26ed3-116">Requirements</span></span>



| <span data-ttu-id="26ed3-117">需求</span><span class="sxs-lookup"><span data-stu-id="26ed3-117">Requirement</span></span> | <span data-ttu-id="26ed3-118">值</span><span class="sxs-lookup"><span data-stu-id="26ed3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26ed3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26ed3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26ed3-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26ed3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26ed3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26ed3-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26ed3-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="26ed3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="26ed3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ed3-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="26ed3-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ed3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26ed3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ed3-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="26ed3-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




