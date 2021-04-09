---
title: 'MCI_VCR_SETVIDEO_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ SETVIDEO \_ PARMS 結構包含適用于 \_ video-卡帶燒錄機之 mci SETVIDEO 命令的參數。
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844160"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="e9fae-104">MCI \_ VCR \_ SETVIDEO \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="e9fae-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="e9fae-105">**Mci \_ VCR \_ SETVIDEO \_ PARMS** 結構包含適用于 video-卡帶燒錄機之 [**mci \_ SETVIDEO**](mci-setvideo.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="e9fae-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fae-106">語法</span><span class="sxs-lookup"><span data-stu-id="e9fae-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="e9fae-107">成員</span><span class="sxs-lookup"><span data-stu-id="e9fae-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9fae-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="e9fae-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="e9fae-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e9fae-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="e9fae-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="e9fae-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="e9fae-111">受影響的曲目。</span><span class="sxs-lookup"><span data-stu-id="e9fae-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="e9fae-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="e9fae-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="e9fae-113">輸入或受監視輸入的類型。</span><span class="sxs-lookup"><span data-stu-id="e9fae-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="e9fae-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="e9fae-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e9fae-115">要使用的 **dwTo** 成員) 中所指定類型的影片輸入 (。</span><span class="sxs-lookup"><span data-stu-id="e9fae-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9fae-116">備註</span><span class="sxs-lookup"><span data-stu-id="e9fae-116">Remarks</span></span>

<span data-ttu-id="e9fae-117">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="e9fae-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9fae-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9fae-118">Requirements</span></span>



| <span data-ttu-id="e9fae-119">需求</span><span class="sxs-lookup"><span data-stu-id="e9fae-119">Requirement</span></span> | <span data-ttu-id="e9fae-120">值</span><span class="sxs-lookup"><span data-stu-id="e9fae-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e9fae-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9fae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9fae-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9fae-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e9fae-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9fae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9fae-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9fae-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e9fae-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e9fae-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9fae-126"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="e9fae-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9fae-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9fae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9fae-128">**Mci**</span><span class="sxs-lookup"><span data-stu-id="e9fae-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e9fae-129">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="e9fae-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="e9fae-130">**MCI \_ SETVIDEO**</span><span class="sxs-lookup"><span data-stu-id="e9fae-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="e9fae-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9fae-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

