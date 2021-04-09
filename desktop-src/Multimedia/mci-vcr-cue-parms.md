---
title: 'MCI_VCR_CUE_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 提示 \_ PARMS 結構包含適用于 \_ 視頻磁帶燒錄機之 MCI 提示命令的參數。
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- MCI_VCR_CUE_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844228"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="f9d44-104">MCI \_ VCR \_ 提示 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="f9d44-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="f9d44-105">**Mci \_ VCR \_ 提示 \_ PARMS** 結構包含適用于視頻磁帶燒錄機之 [**MCI \_ 提示**](mci-cue.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="f9d44-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d44-106">語法</span><span class="sxs-lookup"><span data-stu-id="f9d44-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="f9d44-107">成員</span><span class="sxs-lookup"><span data-stu-id="f9d44-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9d44-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="f9d44-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="f9d44-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f9d44-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="f9d44-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="f9d44-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="f9d44-111">提示來源的位置。</span><span class="sxs-lookup"><span data-stu-id="f9d44-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="f9d44-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="f9d44-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="f9d44-113">要提示的位置。</span><span class="sxs-lookup"><span data-stu-id="f9d44-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9d44-114">備註</span><span class="sxs-lookup"><span data-stu-id="f9d44-114">Remarks</span></span>

<span data-ttu-id="f9d44-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="f9d44-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d44-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d44-116">Requirements</span></span>



| <span data-ttu-id="f9d44-117">需求</span><span class="sxs-lookup"><span data-stu-id="f9d44-117">Requirement</span></span> | <span data-ttu-id="f9d44-118">值</span><span class="sxs-lookup"><span data-stu-id="f9d44-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f9d44-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9d44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d44-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9d44-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f9d44-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9d44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d44-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9d44-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f9d44-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f9d44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9d44-124"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="f9d44-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9d44-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9d44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d44-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="f9d44-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f9d44-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="f9d44-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="f9d44-128">**MCI \_ 提示**</span><span class="sxs-lookup"><span data-stu-id="f9d44-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="f9d44-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9d44-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

