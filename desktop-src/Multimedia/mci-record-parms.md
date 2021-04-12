---
title: 'MCI_RECORD_PARMS 結構 (Mciapi .h) '
description: MCI \_ 記錄 \_ PARMS 結構包含 mci 記錄命令的位置資訊 \_ 。
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464221"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="db887-104">MCI \_ 記錄 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="db887-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="db887-105">**Mci \_ 記錄 \_ PARMS** 結構包含 [**mci \_ 記錄**](mci-record.md)命令的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="db887-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="db887-106">語法</span><span class="sxs-lookup"><span data-stu-id="db887-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="db887-107">成員</span><span class="sxs-lookup"><span data-stu-id="db887-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="db887-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="db887-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="db887-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="db887-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="db887-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="db887-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="db887-111">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="db887-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="db887-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="db887-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="db887-113">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="db887-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db887-114">備註</span><span class="sxs-lookup"><span data-stu-id="db887-114">Remarks</span></span>

<span data-ttu-id="db887-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="db887-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="db887-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="db887-116">Requirements</span></span>



| <span data-ttu-id="db887-117">需求</span><span class="sxs-lookup"><span data-stu-id="db887-117">Requirement</span></span> | <span data-ttu-id="db887-118">值</span><span class="sxs-lookup"><span data-stu-id="db887-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db887-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db887-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db887-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db887-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="db887-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db887-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db887-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db887-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="db887-123">標頭</span><span class="sxs-lookup"><span data-stu-id="db887-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db887-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="db887-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db887-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db887-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db887-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="db887-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="db887-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="db887-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="db887-128">**MCI \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="db887-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="db887-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db887-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

