---
title: 'MCI_VCR_SETAUDIO_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ SETAUDIO \_ PARMS 結構包含適用于 \_ video-卡帶燒錄機之 mci SETAUDIO 命令的參數。
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843200"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="8a769-104">MCI \_ VCR \_ SETAUDIO \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="8a769-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="8a769-105">**Mci \_ VCR \_ SETAUDIO \_ PARMS** 結構包含適用于 video-卡帶燒錄機之 [**mci \_ SETAUDIO**](mci-setaudio.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="8a769-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a769-106">語法</span><span class="sxs-lookup"><span data-stu-id="8a769-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="8a769-107">成員</span><span class="sxs-lookup"><span data-stu-id="8a769-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a769-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8a769-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8a769-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8a769-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8a769-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="8a769-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="8a769-111">音訊播放軌。</span><span class="sxs-lookup"><span data-stu-id="8a769-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="8a769-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="8a769-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="8a769-113">輸入或受監視輸入的類型。</span><span class="sxs-lookup"><span data-stu-id="8a769-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="8a769-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="8a769-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="8a769-115">要使用的 **dwTo** 成員) 中所指定類型的音訊輸入 (。</span><span class="sxs-lookup"><span data-stu-id="8a769-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a769-116">備註</span><span class="sxs-lookup"><span data-stu-id="8a769-116">Remarks</span></span>

<span data-ttu-id="8a769-117">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="8a769-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a769-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a769-118">Requirements</span></span>



| <span data-ttu-id="8a769-119">需求</span><span class="sxs-lookup"><span data-stu-id="8a769-119">Requirement</span></span> | <span data-ttu-id="8a769-120">值</span><span class="sxs-lookup"><span data-stu-id="8a769-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8a769-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a769-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a769-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a769-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8a769-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a769-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a769-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a769-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8a769-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8a769-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a769-126"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="8a769-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a769-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a769-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a769-128">**Mci**</span><span class="sxs-lookup"><span data-stu-id="8a769-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8a769-129">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="8a769-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8a769-130">**MCI \_ SETAUDIO**</span><span class="sxs-lookup"><span data-stu-id="8a769-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="8a769-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a769-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

