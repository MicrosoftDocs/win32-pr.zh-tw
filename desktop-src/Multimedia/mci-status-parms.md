---
title: 'MCI_STATUS_PARMS 結構 (Mciapi .h) '
description: MCI \_ status \_ PARMS 結構包含 mci status 命令的資訊 \_ 。
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934031"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="b7de1-104">MCI \_ 狀態 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="b7de1-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="b7de1-105">**Mci \_ status \_ PARMS** 結構包含 [**mci \_ status**](mci-status.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="b7de1-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7de1-106">語法</span><span class="sxs-lookup"><span data-stu-id="b7de1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="b7de1-107">成員</span><span class="sxs-lookup"><span data-stu-id="b7de1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7de1-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="b7de1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b7de1-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b7de1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b7de1-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="b7de1-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="b7de1-111">包含傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="b7de1-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="b7de1-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="b7de1-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="b7de1-113">正在查詢的功能。</span><span class="sxs-lookup"><span data-stu-id="b7de1-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="b7de1-114">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="b7de1-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="b7de1-115">曲目的長度或數目。</span><span class="sxs-lookup"><span data-stu-id="b7de1-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7de1-116">備註</span><span class="sxs-lookup"><span data-stu-id="b7de1-116">Remarks</span></span>

<span data-ttu-id="b7de1-117">您 \_ \_ 必須在 [**MciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定 MCI 狀態專案旗標，以驗證 **dwItem** 成員，其中應包含其中一個表示要求狀態資訊的常數。</span><span class="sxs-lookup"><span data-stu-id="b7de1-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7de1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7de1-118">Requirements</span></span>



| <span data-ttu-id="b7de1-119">需求</span><span class="sxs-lookup"><span data-stu-id="b7de1-119">Requirement</span></span> | <span data-ttu-id="b7de1-120">值</span><span class="sxs-lookup"><span data-stu-id="b7de1-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b7de1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7de1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7de1-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7de1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b7de1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7de1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7de1-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7de1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7de1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b7de1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7de1-126"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7de1-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7de1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7de1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7de1-128">**Mci**</span><span class="sxs-lookup"><span data-stu-id="b7de1-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b7de1-129">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="b7de1-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b7de1-130">**MCI \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="b7de1-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="b7de1-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7de1-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

