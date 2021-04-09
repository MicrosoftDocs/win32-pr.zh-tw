---
title: 'MCI_VCR_STEP_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 步驟 \_ PARMS 結構包含適用于 \_ video/卡帶燒錄機之 mci 步驟命令的參數。
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024707"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="8010e-104">MCI \_ VCR \_ 步驟 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="8010e-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="8010e-105">**Mci \_ VCR \_ 步驟 \_ PARMS** 結構包含適用于 video/卡帶燒錄機 [**之 mci \_ 步驟**](mci-step.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="8010e-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="8010e-106">語法</span><span class="sxs-lookup"><span data-stu-id="8010e-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="8010e-107">成員</span><span class="sxs-lookup"><span data-stu-id="8010e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8010e-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8010e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8010e-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8010e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8010e-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="8010e-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="8010e-111">要跳過的畫面格數目 (單一步驟的長度，) 為在內容中向前或向後執行的步驟。 [**\_**](mci-step.md)</span><span class="sxs-lookup"><span data-stu-id="8010e-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8010e-112">備註</span><span class="sxs-lookup"><span data-stu-id="8010e-112">Remarks</span></span>

<span data-ttu-id="8010e-113">將資料指派給此結構中的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="8010e-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8010e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8010e-114">Requirements</span></span>



| <span data-ttu-id="8010e-115">需求</span><span class="sxs-lookup"><span data-stu-id="8010e-115">Requirement</span></span> | <span data-ttu-id="8010e-116">值</span><span class="sxs-lookup"><span data-stu-id="8010e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8010e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8010e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8010e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8010e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8010e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8010e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8010e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8010e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8010e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8010e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8010e-122"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="8010e-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8010e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8010e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8010e-124">**Mci**</span><span class="sxs-lookup"><span data-stu-id="8010e-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8010e-125">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="8010e-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8010e-126">**MCI \_ 步驟**</span><span class="sxs-lookup"><span data-stu-id="8010e-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="8010e-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8010e-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

