---
title: 'MCI_VCR_SEEK_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 搜尋 \_ PARMS 結構包含適用于 video 的 mci \_ 搜尋命令的參數。
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464833"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="9047d-104">MCI \_ VCR \_ 搜尋 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="9047d-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="9047d-105">**Mci \_ VCR \_ 搜尋 \_ PARMS** 結構包含適用于 video 的 [**mci \_ 搜尋**](mci-seek.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="9047d-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="9047d-106">語法</span><span class="sxs-lookup"><span data-stu-id="9047d-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="9047d-107">成員</span><span class="sxs-lookup"><span data-stu-id="9047d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9047d-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="9047d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="9047d-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9047d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="9047d-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="9047d-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="9047d-111">要搜尋的位置。</span><span class="sxs-lookup"><span data-stu-id="9047d-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="9047d-112">**dwMark**</span><span class="sxs-lookup"><span data-stu-id="9047d-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="9047d-113">要搜尋的編號標記。</span><span class="sxs-lookup"><span data-stu-id="9047d-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="9047d-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="9047d-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="9047d-115">開始搜尋的時間。</span><span class="sxs-lookup"><span data-stu-id="9047d-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9047d-116">備註</span><span class="sxs-lookup"><span data-stu-id="9047d-116">Remarks</span></span>

<span data-ttu-id="9047d-117">以目前時間格式指定位置。</span><span class="sxs-lookup"><span data-stu-id="9047d-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="9047d-118">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="9047d-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9047d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9047d-119">Requirements</span></span>



| <span data-ttu-id="9047d-120">需求</span><span class="sxs-lookup"><span data-stu-id="9047d-120">Requirement</span></span> | <span data-ttu-id="9047d-121">值</span><span class="sxs-lookup"><span data-stu-id="9047d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9047d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9047d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9047d-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9047d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9047d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9047d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9047d-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9047d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9047d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9047d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9047d-127"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="9047d-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9047d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9047d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9047d-129">**Mci**</span><span class="sxs-lookup"><span data-stu-id="9047d-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9047d-130">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="9047d-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="9047d-131">**MCI \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="9047d-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="9047d-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9047d-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

