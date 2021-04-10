---
title: 'MCI_SEQ_SET_PARMS 結構 (Mciapi .h) '
description: MCI \_ SEQ \_ set \_ PARMS 結構包含適用于 \_ MIDI sequencer 裝置之 MCI SET 命令的資訊。
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934032"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="16922-104">MCI \_ SEQ \_ SET \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="16922-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="16922-105">**Mci \_ SEQ \_ set \_ PARMS** 結構包含適用于 MIDI sequencer 裝置之 [**MCI \_ SET**](mci-set.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="16922-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="16922-106">語法</span><span class="sxs-lookup"><span data-stu-id="16922-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="16922-107">成員</span><span class="sxs-lookup"><span data-stu-id="16922-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="16922-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="16922-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="16922-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="16922-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="16922-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="16922-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="16922-111">Sequencer 的時間格式。</span><span class="sxs-lookup"><span data-stu-id="16922-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="16922-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="16922-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="16922-113">音訊輸出通道。</span><span class="sxs-lookup"><span data-stu-id="16922-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="16922-114">**dwTempo**</span><span class="sxs-lookup"><span data-stu-id="16922-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="16922-115">節奏。</span><span class="sxs-lookup"><span data-stu-id="16922-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="16922-116">**dwPort**</span><span class="sxs-lookup"><span data-stu-id="16922-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="16922-117">連接埠。</span><span class="sxs-lookup"><span data-stu-id="16922-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="16922-118">**dwSlave**</span><span class="sxs-lookup"><span data-stu-id="16922-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="16922-119">排序器針對次級作業所使用的同步處理類型。</span><span class="sxs-lookup"><span data-stu-id="16922-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="16922-120">**dwMaster**</span><span class="sxs-lookup"><span data-stu-id="16922-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="16922-121">排序器針對主要作業所使用的同步處理類型。</span><span class="sxs-lookup"><span data-stu-id="16922-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="16922-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="16922-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="16922-123">資料位移。</span><span class="sxs-lookup"><span data-stu-id="16922-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16922-124">備註</span><span class="sxs-lookup"><span data-stu-id="16922-124">Remarks</span></span>

<span data-ttu-id="16922-125">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="16922-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="16922-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="16922-126">Requirements</span></span>



| <span data-ttu-id="16922-127">需求</span><span class="sxs-lookup"><span data-stu-id="16922-127">Requirement</span></span> | <span data-ttu-id="16922-128">值</span><span class="sxs-lookup"><span data-stu-id="16922-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16922-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16922-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16922-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16922-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="16922-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16922-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16922-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16922-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16922-133">標頭</span><span class="sxs-lookup"><span data-stu-id="16922-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="16922-134"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="16922-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16922-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16922-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16922-136">**Mci**</span><span class="sxs-lookup"><span data-stu-id="16922-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="16922-137">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="16922-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="16922-138">**MCI \_ 組**</span><span class="sxs-lookup"><span data-stu-id="16922-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="16922-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16922-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

