---
description: 搭配使用 IOCTL \_ SCSI \_ 微型埠 IOCTL 和 CTLCODE \_ ISCSITGT \_ SPT \_ SESSION \_ END (0x101) 控制程式代碼來停止會話。
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: ISCSITGT_SPT_SESSION_STOP 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "103853556"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="a2593-103">ISCSITGT \_ SPT \_ 會話 \_ 停止結構</span><span class="sxs-lookup"><span data-stu-id="a2593-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="a2593-104">\[以下是可在 Windows Server 2012 R2 中使用的結構。</span><span class="sxs-lookup"><span data-stu-id="a2593-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="a2593-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a2593-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="a2593-106">搭配使用 [**IOCTL \_ SCSI \_ 微型埠**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) ioctl 和 CTLCODE \_ ISCSITGT \_ SPT \_ SESSION \_ END (0x101) 控制程式代碼來停止會話。</span><span class="sxs-lookup"><span data-stu-id="a2593-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2593-107">語法</span><span class="sxs-lookup"><span data-stu-id="a2593-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="a2593-108">成員</span><span class="sxs-lookup"><span data-stu-id="a2593-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2593-109">**標頭**</span><span class="sxs-lookup"><span data-stu-id="a2593-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="a2593-110">必要標頭。</span><span class="sxs-lookup"><span data-stu-id="a2593-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="a2593-111">**ITNexusHandle**</span><span class="sxs-lookup"><span data-stu-id="a2593-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a2593-112">代表會話的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="a2593-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2593-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2593-113">Requirements</span></span>



| <span data-ttu-id="a2593-114">需求</span><span class="sxs-lookup"><span data-stu-id="a2593-114">Requirement</span></span> | <span data-ttu-id="a2593-115">值</span><span class="sxs-lookup"><span data-stu-id="a2593-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a2593-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2593-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2593-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="a2593-117">None supported</span></span><br/>                               |
| <span data-ttu-id="a2593-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2593-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2593-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2593-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a2593-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a2593-120">End of client support</span></span><br/>    | <span data-ttu-id="a2593-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="a2593-121">None supported</span></span><br/>                               |
| <span data-ttu-id="a2593-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a2593-122">End of server support</span></span><br/>    | <span data-ttu-id="a2593-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a2593-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a2593-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2593-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2593-125">iSCSI 目標傳遞</span><span class="sxs-lookup"><span data-stu-id="a2593-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="a2593-126">**SRB \_ IO \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="a2593-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
