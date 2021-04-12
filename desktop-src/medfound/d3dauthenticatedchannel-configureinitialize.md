---
description: 包含 D3DAUTHENTICATEDCONFIGURE INITIALIZE 命令的輸入資料 \_ 。
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026047"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="f5c0d-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE 結構</span><span class="sxs-lookup"><span data-stu-id="f5c0d-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="f5c0d-104">包含 [**D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE**](d3dauthenticatedconfigure-initialize.md) 命令的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="f5c0d-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c0d-106">語法</span><span class="sxs-lookup"><span data-stu-id="f5c0d-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="f5c0d-107">成員</span><span class="sxs-lookup"><span data-stu-id="f5c0d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5c0d-108">**參數**</span><span class="sxs-lookup"><span data-stu-id="f5c0d-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="f5c0d-109">D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="f5c0d-110">**StartSequenceQuery**</span><span class="sxs-lookup"><span data-stu-id="f5c0d-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="f5c0d-111">查詢的初始序號。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="f5c0d-112">**StartSequenceConfigure**</span><span class="sxs-lookup"><span data-stu-id="f5c0d-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="f5c0d-113">命令的初始序號。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5c0d-114">備註</span><span class="sxs-lookup"><span data-stu-id="f5c0d-114">Remarks</span></span>

<span data-ttu-id="f5c0d-115">**StartSequenceQuery** 和 **StartSequenceConfigure** 成員都包含密碼編譯安全32位的亂數字。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c0d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5c0d-116">Requirements</span></span>



| <span data-ttu-id="f5c0d-117">需求</span><span class="sxs-lookup"><span data-stu-id="f5c0d-117">Requirement</span></span> | <span data-ttu-id="f5c0d-118">值</span><span class="sxs-lookup"><span data-stu-id="f5c0d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c0d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5c0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c0d-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5c0d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5c0d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5c0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c0d-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5c0d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f5c0d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f5c0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c0d-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c0d-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c0d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5c0d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c0d-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="f5c0d-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f5c0d-127">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="f5c0d-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




