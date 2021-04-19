---
description: 包含 D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE 命令的輸入資料 \_ 。
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991662"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="e0302-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE 結構</span><span class="sxs-lookup"><span data-stu-id="e0302-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="e0302-104">包含 [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) 命令的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="e0302-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="e0302-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。</span><span class="sxs-lookup"><span data-stu-id="e0302-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0302-106">語法</span><span class="sxs-lookup"><span data-stu-id="e0302-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="e0302-107">成員</span><span class="sxs-lookup"><span data-stu-id="e0302-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0302-108">**參數**</span><span class="sxs-lookup"><span data-stu-id="e0302-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="e0302-109">D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0302-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="e0302-110">**ProcessIdentiferType**</span><span class="sxs-lookup"><span data-stu-id="e0302-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="e0302-111">指定進程類型的 [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="e0302-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="e0302-112">若要指定桌面視窗管理員 (DWM) 進程，請將這個成員設定為 **PROCESSIDTYPE \_ dwm**。</span><span class="sxs-lookup"><span data-stu-id="e0302-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="e0302-113">否則，請將這個成員設定為 **PROCESSIDTYPE \_ 控制碼** ，並將 **ProcessHandle** 成員設定為有效的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0302-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="e0302-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="e0302-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e0302-115">進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0302-115">A process handle.</span></span> <span data-ttu-id="e0302-116">如果 **ProcessIdentifier** 成員等於 **PROCESSTIDTYPE \_ 控制碼**， **ProcessHandle** 成員會指定進程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0302-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="e0302-117">否則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="e0302-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="e0302-118">**AllowAccess**</span><span class="sxs-lookup"><span data-stu-id="e0302-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="e0302-119">若 **為 TRUE**，表示指定的進程可以存取受限制的共用資源。</span><span class="sxs-lookup"><span data-stu-id="e0302-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0302-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0302-120">Requirements</span></span>



| <span data-ttu-id="e0302-121">需求</span><span class="sxs-lookup"><span data-stu-id="e0302-121">Requirement</span></span> | <span data-ttu-id="e0302-122">值</span><span class="sxs-lookup"><span data-stu-id="e0302-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0302-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0302-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e0302-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0302-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e0302-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0302-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e0302-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0302-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e0302-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e0302-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0302-128"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0302-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0302-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0302-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0302-130">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="e0302-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e0302-131">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="e0302-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




