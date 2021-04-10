---
title: 'MCI_VCR_STATUS_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ status \_ PARMS 結構包含適用于 \_ video/磁帶燒錄機的 mci status 命令參數。
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933983"
---
# <a name="mci_vcr_status_parms-structure"></a><span data-ttu-id="5d9af-104">MCI \_ VCR \_ 狀態 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="5d9af-104">MCI\_VCR\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="5d9af-105">**Mci \_ VCR \_ status \_ PARMS** 結構包含適用于 video/磁帶燒錄機的 [**mci \_ status**](mci-status.md)命令參數。</span><span class="sxs-lookup"><span data-stu-id="5d9af-105">The **MCI\_VCR\_STATUS\_PARMS** structure contains parameters for the [**MCI\_STATUS**](mci-status.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d9af-106">語法</span><span class="sxs-lookup"><span data-stu-id="5d9af-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="5d9af-107">成員</span><span class="sxs-lookup"><span data-stu-id="5d9af-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d9af-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="5d9af-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="5d9af-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5d9af-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="5d9af-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="5d9af-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="5d9af-111">[**MCI \_ STATUS**](mci-status.md)命令所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="5d9af-111">Value returned by the [**MCI\_STATUS**](mci-status.md) command.</span></span> <span data-ttu-id="5d9af-112">傳回值會根據命令的查詢而有所不同。</span><span class="sxs-lookup"><span data-stu-id="5d9af-112">The return value varies according to the inquiry of the command.</span></span> <span data-ttu-id="5d9af-113">如需詳細資訊，請參閱 [**MCI \_ STATUS**](mci-status-parms.md) 命令的描述。</span><span class="sxs-lookup"><span data-stu-id="5d9af-113">For more information, see the description of the [**MCI\_STATUS**](mci-status-parms.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="5d9af-114">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="5d9af-114">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="5d9af-115">要求的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="5d9af-115">Type of information requested.</span></span>

</dd> <dt>

<span data-ttu-id="5d9af-116">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="5d9af-116">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="5d9af-117">將在下次錄製期間儲存資訊的音訊或影片播放軌。</span><span class="sxs-lookup"><span data-stu-id="5d9af-117">Audio or video track that will store information during the next recording.</span></span> <span data-ttu-id="5d9af-118">當 [**MCI \_ STATUS**](mci-status-parms.md) 命令查詢影片或音訊錄製狀態時，此成員會用來傳回信息。</span><span class="sxs-lookup"><span data-stu-id="5d9af-118">This member is used to return information when the [**MCI\_STATUS**](mci-status-parms.md) command inquires about the video or audio recording status.</span></span>

</dd> <dt>

<span data-ttu-id="5d9af-119">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="5d9af-119">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5d9af-120">與目前通道相關聯的邏輯調諧器。</span><span class="sxs-lookup"><span data-stu-id="5d9af-120">Logical tuner that the current channel is associated with.</span></span> <span data-ttu-id="5d9af-121">當 [**MCI \_ STATUS**](mci-status.md) 命令查詢目前的通道號碼時，此成員會用來傳回信息。</span><span class="sxs-lookup"><span data-stu-id="5d9af-121">This member is used to return information when the [**MCI\_STATUS**](mci-status.md) command inquires about the current channel number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d9af-122">備註</span><span class="sxs-lookup"><span data-stu-id="5d9af-122">Remarks</span></span>

<span data-ttu-id="5d9af-123">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="5d9af-123">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d9af-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d9af-124">Requirements</span></span>



| <span data-ttu-id="5d9af-125">需求</span><span class="sxs-lookup"><span data-stu-id="5d9af-125">Requirement</span></span> | <span data-ttu-id="5d9af-126">值</span><span class="sxs-lookup"><span data-stu-id="5d9af-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d9af-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d9af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d9af-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d9af-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5d9af-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d9af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d9af-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d9af-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d9af-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5d9af-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d9af-132"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="5d9af-132"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d9af-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d9af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d9af-134">**Mci**</span><span class="sxs-lookup"><span data-stu-id="5d9af-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5d9af-135">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="5d9af-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="5d9af-136">**MCI \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="5d9af-136">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="5d9af-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d9af-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

