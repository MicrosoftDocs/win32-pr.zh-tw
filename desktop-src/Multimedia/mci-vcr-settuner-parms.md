---
title: 'MCI_VCR_SETTUNER_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ SETTUNER \_ PARMS 結構包含適用于 \_ video-卡帶燒錄機之 mci SETTUNER 命令的參數。
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- MCI_VCR_SETTUNER_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685983"
---
# <a name="mci_vcr_settuner_parms-structure"></a><span data-ttu-id="11ce8-104">MCI \_ VCR \_ SETTUNER \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="11ce8-104">MCI\_VCR\_SETTUNER\_PARMS structure</span></span>

<span data-ttu-id="11ce8-105">**Mci \_ VCR \_ SETTUNER \_ PARMS** 結構包含適用于 video-卡帶燒錄機之 [**mci \_ SETTUNER**](mci-settuner.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="11ce8-105">The **MCI\_VCR\_SETTUNER\_PARMS** structure contains parameters for the [**MCI\_SETTUNER**](mci-settuner.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ce8-106">語法</span><span class="sxs-lookup"><span data-stu-id="11ce8-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a><span data-ttu-id="11ce8-107">成員</span><span class="sxs-lookup"><span data-stu-id="11ce8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="11ce8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="11ce8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="11ce8-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="11ce8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="11ce8-110">**dwChannel**</span><span class="sxs-lookup"><span data-stu-id="11ce8-110">**dwChannel**</span></span>
</dt> <dd>

<span data-ttu-id="11ce8-111">新頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="11ce8-111">New channel number.</span></span>

</dd> <dt>

<span data-ttu-id="11ce8-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="11ce8-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="11ce8-113">[**MCI \_ SETTUNER**](mci-settuner.md)命令影響的邏輯調諧器。</span><span class="sxs-lookup"><span data-stu-id="11ce8-113">Logical tuner that the [**MCI\_SETTUNER**](mci-settuner.md) command affects.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11ce8-114">備註</span><span class="sxs-lookup"><span data-stu-id="11ce8-114">Remarks</span></span>

<span data-ttu-id="11ce8-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="11ce8-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ce8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="11ce8-116">Requirements</span></span>



| <span data-ttu-id="11ce8-117">需求</span><span class="sxs-lookup"><span data-stu-id="11ce8-117">Requirement</span></span> | <span data-ttu-id="11ce8-118">值</span><span class="sxs-lookup"><span data-stu-id="11ce8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="11ce8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11ce8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="11ce8-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11ce8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="11ce8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11ce8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="11ce8-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11ce8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="11ce8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="11ce8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11ce8-124"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="11ce8-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ce8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11ce8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ce8-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="11ce8-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="11ce8-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="11ce8-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="11ce8-128">**MCI \_ SETTUNER**</span><span class="sxs-lookup"><span data-stu-id="11ce8-128">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
</dt> <dt>

<span data-ttu-id="11ce8-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11ce8-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

