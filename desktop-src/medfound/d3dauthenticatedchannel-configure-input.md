---
description: 包含 IDirect3DAuthenticatedChannel9：： Configure 方法的輸入資料。
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191072"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="6b57d-103">D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="6b57d-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="6b57d-104">包含 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="6b57d-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b57d-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b57d-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="6b57d-106">成員</span><span class="sxs-lookup"><span data-stu-id="6b57d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b57d-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="6b57d-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="6b57d-108">[**D3D \_ OMAC**](d3d-omac.md)結構，其中包含資料的訊息驗證碼 (MAC) 。</span><span class="sxs-lookup"><span data-stu-id="6b57d-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="6b57d-109">驅動程式會使用 AES 型單鍵 CBC MAC (OMAC) 為此結構成員後面出現的資料區塊計算此值。</span><span class="sxs-lookup"><span data-stu-id="6b57d-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="6b57d-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="6b57d-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="6b57d-111">指定命令的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6b57d-111">A GUID that specifies the command.</span></span> <span data-ttu-id="6b57d-112">如需值的清單，請參閱 [內容保護命令](content-protection-commands.md)。</span><span class="sxs-lookup"><span data-stu-id="6b57d-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b57d-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="6b57d-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="6b57d-114">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6b57d-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="6b57d-115">若要取得控制碼，請呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="6b57d-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="6b57d-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="6b57d-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6b57d-117">查詢序號。</span><span class="sxs-lookup"><span data-stu-id="6b57d-117">The query sequence number.</span></span> <span data-ttu-id="6b57d-118">在會話開始時，產生以密碼編譯的安全32位亂數字，作為起始序號使用。</span><span class="sxs-lookup"><span data-stu-id="6b57d-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="6b57d-119">針對每個命令，將序號遞增1。</span><span class="sxs-lookup"><span data-stu-id="6b57d-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b57d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b57d-120">Requirements</span></span>



| <span data-ttu-id="6b57d-121">需求</span><span class="sxs-lookup"><span data-stu-id="6b57d-121">Requirement</span></span> | <span data-ttu-id="6b57d-122">值</span><span class="sxs-lookup"><span data-stu-id="6b57d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b57d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b57d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b57d-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b57d-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6b57d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b57d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b57d-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b57d-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b57d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6b57d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b57d-128"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b57d-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b57d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b57d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b57d-130">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="6b57d-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="6b57d-131">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="6b57d-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




