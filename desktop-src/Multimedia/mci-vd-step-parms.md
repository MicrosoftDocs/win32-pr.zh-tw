---
title: 'MCI_VD_STEP_PARMS 結構 (Mciapi .h) '
description: MCI \_ VD \_ step \_ PARMS 結構包含適用于 \_ videodisc 裝置之 MCI 步驟命令的資訊。
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- MCI_VD_STEP_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508599"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="6bbbf-104">MCI \_ VD \_ 步驟 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="6bbbf-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="6bbbf-105">**Mci \_ VD \_ step \_ PARMS** 結構包含適用于 videodisc 裝置 [**之 MCI \_ 步驟**](mci-step.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="6bbbf-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbbf-106">語法</span><span class="sxs-lookup"><span data-stu-id="6bbbf-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="6bbbf-107">成員</span><span class="sxs-lookup"><span data-stu-id="6bbbf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6bbbf-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6bbbf-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6bbbf-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6bbbf-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6bbbf-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="6bbbf-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="6bbbf-111">要逐步執行的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="6bbbf-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bbbf-112">備註</span><span class="sxs-lookup"><span data-stu-id="6bbbf-112">Remarks</span></span>

<span data-ttu-id="6bbbf-113">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="6bbbf-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bbbf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bbbf-114">Requirements</span></span>



| <span data-ttu-id="6bbbf-115">需求</span><span class="sxs-lookup"><span data-stu-id="6bbbf-115">Requirement</span></span> | <span data-ttu-id="6bbbf-116">值</span><span class="sxs-lookup"><span data-stu-id="6bbbf-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbbf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bbbf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6bbbf-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bbbf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6bbbf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bbbf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6bbbf-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bbbf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6bbbf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6bbbf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bbbf-122"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bbbf-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bbbf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bbbf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbbf-124">**Mci**</span><span class="sxs-lookup"><span data-stu-id="6bbbf-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6bbbf-125">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="6bbbf-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6bbbf-126">**MCI \_ 步驟**</span><span class="sxs-lookup"><span data-stu-id="6bbbf-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="6bbbf-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6bbbf-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

