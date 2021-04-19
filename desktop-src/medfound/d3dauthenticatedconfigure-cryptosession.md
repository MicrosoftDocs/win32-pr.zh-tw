---
description: 將密碼編譯會話與 DirectX Video 加速 2 (DXVA-2) 解碼器裝置和 Direct3D 裝置產生關聯。
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: 'D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972153"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="6bc1e-103">D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="6bc1e-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="6bc1e-104">將密碼編譯會話與 DirectX Video 加速 2 (DXVA-2) 解碼器裝置和 Direct3D 裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6bc1e-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="6bc1e-105">需求</span><span class="sxs-lookup"><span data-stu-id="6bc1e-105">Requirement</span></span> | <span data-ttu-id="6bc1e-106">值</span><span class="sxs-lookup"><span data-stu-id="6bc1e-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc1e-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="6bc1e-107">Command GUID</span></span> | <span data-ttu-id="6bc1e-108">**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="6bc1e-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="6bc1e-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="6bc1e-109">Input data</span></span>   | [<span data-ttu-id="6bc1e-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="6bc1e-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="6bc1e-111">備註</span><span class="sxs-lookup"><span data-stu-id="6bc1e-111">Remarks</span></span>

<span data-ttu-id="6bc1e-112">傳送這個命令之後，您可以傳送 [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) 查詢，找出哪些影片輸出與密碼編譯會話相關聯。</span><span class="sxs-lookup"><span data-stu-id="6bc1e-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="6bc1e-113">下列通道類型支援此命令：</span><span class="sxs-lookup"><span data-stu-id="6bc1e-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="6bc1e-114">**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="6bc1e-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="6bc1e-115">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="6bc1e-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc1e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bc1e-116">Requirements</span></span>



| <span data-ttu-id="6bc1e-117">需求</span><span class="sxs-lookup"><span data-stu-id="6bc1e-117">Requirement</span></span> | <span data-ttu-id="6bc1e-118">值</span><span class="sxs-lookup"><span data-stu-id="6bc1e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc1e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bc1e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc1e-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bc1e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6bc1e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bc1e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc1e-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bc1e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6bc1e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6bc1e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bc1e-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bc1e-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bc1e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bc1e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc1e-126">內容保護命令</span><span class="sxs-lookup"><span data-stu-id="6bc1e-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="6bc1e-127">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="6bc1e-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="6bc1e-128">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="6bc1e-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




