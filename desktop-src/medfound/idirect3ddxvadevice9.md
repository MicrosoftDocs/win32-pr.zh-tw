---
description: 代表 DirectX Video 加速的硬體加速器 (DXVA) 1.0。
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: 'IDirect3DDXVADevice9 介面 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974408"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="d43f9-103">IDirect3DDXVADevice9 介面</span><span class="sxs-lookup"><span data-stu-id="d43f9-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="d43f9-104">代表 DirectX Video 加速的硬體加速器 (DXVA) 1.0。</span><span class="sxs-lookup"><span data-stu-id="d43f9-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="d43f9-105">成員</span><span class="sxs-lookup"><span data-stu-id="d43f9-105">Members</span></span>

<span data-ttu-id="d43f9-106">**IDirect3DDXVADevice9** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d43f9-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d43f9-107">**IDirect3DDXVADevice9** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d43f9-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="d43f9-108">方法</span><span class="sxs-lookup"><span data-stu-id="d43f9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d43f9-109">方法</span><span class="sxs-lookup"><span data-stu-id="d43f9-109">Methods</span></span>

<span data-ttu-id="d43f9-110">**IDirect3DDXVADevice9** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d43f9-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="d43f9-111">方法</span><span class="sxs-lookup"><span data-stu-id="d43f9-111">Method</span></span>                                                  | <span data-ttu-id="d43f9-112">描述</span><span class="sxs-lookup"><span data-stu-id="d43f9-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="d43f9-113">**BeginFrame**</span><span class="sxs-lookup"><span data-stu-id="d43f9-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="d43f9-114">開始處理以建立解碼的圖片。</span><span class="sxs-lookup"><span data-stu-id="d43f9-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="d43f9-115">**EndFrame**</span><span class="sxs-lookup"><span data-stu-id="d43f9-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="d43f9-116">結束處理以建立解碼的圖片。</span><span class="sxs-lookup"><span data-stu-id="d43f9-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="d43f9-117">**執行**</span><span class="sxs-lookup"><span data-stu-id="d43f9-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="d43f9-118">執行 DXVA 解碼作業。</span><span class="sxs-lookup"><span data-stu-id="d43f9-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="d43f9-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="d43f9-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="d43f9-120">查詢 DXVA 解碼介面的讀取/寫入狀態。</span><span class="sxs-lookup"><span data-stu-id="d43f9-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d43f9-121">備註</span><span class="sxs-lookup"><span data-stu-id="d43f9-121">Remarks</span></span>

<span data-ttu-id="d43f9-122">若要取得這個介面的指標，請呼叫 [**IDirect3DVideoDevice9：： CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d43f9-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d43f9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d43f9-123">Requirements</span></span>



| <span data-ttu-id="d43f9-124">需求</span><span class="sxs-lookup"><span data-stu-id="d43f9-124">Requirement</span></span> | <span data-ttu-id="d43f9-125">值</span><span class="sxs-lookup"><span data-stu-id="d43f9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d43f9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d43f9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d43f9-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d43f9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d43f9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d43f9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d43f9-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d43f9-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d43f9-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d43f9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d43f9-131"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="d43f9-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d43f9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d43f9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43f9-133">Direct3D Video 介面</span><span class="sxs-lookup"><span data-stu-id="d43f9-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
