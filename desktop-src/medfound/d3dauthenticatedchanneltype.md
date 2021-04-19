---
description: 指定 Direct3D 驗證通道的類型。
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: 'D3DAUTHENTICATEDCHANNELTYPE 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971982"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="ab52e-103">D3DAUTHENTICATEDCHANNELTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="ab52e-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="ab52e-104">指定 Direct3D 驗證通道的類型。</span><span class="sxs-lookup"><span data-stu-id="ab52e-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab52e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab52e-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="ab52e-106">常數</span><span class="sxs-lookup"><span data-stu-id="ab52e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab52e-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="ab52e-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="ab52e-108">Direct3D 9 通道。</span><span class="sxs-lookup"><span data-stu-id="ab52e-108">Direct3D 9 channel.</span></span> <span data-ttu-id="ab52e-109">此通道會提供與 Direct3D 執行時間的通訊。</span><span class="sxs-lookup"><span data-stu-id="ab52e-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="ab52e-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="ab52e-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ab52e-111">軟體驅動程式通道。</span><span class="sxs-lookup"><span data-stu-id="ab52e-111">Software driver channel.</span></span> <span data-ttu-id="ab52e-112">此通道提供的驅動程式與在軟體中實施內容保護機制的驅動程式通訊。</span><span class="sxs-lookup"><span data-stu-id="ab52e-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="ab52e-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="ab52e-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ab52e-114">硬體驅動程式通道。</span><span class="sxs-lookup"><span data-stu-id="ab52e-114">Hardware driver channel.</span></span> <span data-ttu-id="ab52e-115">此通道可讓您與驅動程式進行通訊，以在 GPU 硬體中執行內容保護機制。</span><span class="sxs-lookup"><span data-stu-id="ab52e-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab52e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab52e-116">Requirements</span></span>



| <span data-ttu-id="ab52e-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab52e-117">Requirement</span></span> | <span data-ttu-id="ab52e-118">值</span><span class="sxs-lookup"><span data-stu-id="ab52e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab52e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab52e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab52e-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab52e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab52e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab52e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab52e-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab52e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ab52e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ab52e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab52e-124"><dt>D3d9types (包含 D3d9) </dt></span><span class="sxs-lookup"><span data-stu-id="ab52e-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab52e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab52e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab52e-126">Direct3D 影片列舉</span><span class="sxs-lookup"><span data-stu-id="ab52e-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="ab52e-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span><span class="sxs-lookup"><span data-stu-id="ab52e-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




