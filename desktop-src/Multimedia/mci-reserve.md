---
title: 'MCI_RESERVE 命令 (Mmsystem .h) '
description: MCI \_ RESERVE 命令會為設備磁碟機實例的工作區配置連續的磁碟空間，以用於後續錄製。 數位影片裝置辨識此命令。
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934842"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="936b5-105">MCI \_ 保留命令</span><span class="sxs-lookup"><span data-stu-id="936b5-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="936b5-106">MCI \_ RESERVE 命令會為設備磁碟機實例的工作區配置連續的磁碟空間，以用於後續錄製。</span><span class="sxs-lookup"><span data-stu-id="936b5-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="936b5-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="936b5-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="936b5-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="936b5-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="936b5-109">參數</span><span class="sxs-lookup"><span data-stu-id="936b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936b5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="936b5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="936b5-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="936b5-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="936b5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="936b5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="936b5-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="936b5-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="936b5-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="936b5-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="936b5-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span><span class="sxs-lookup"><span data-stu-id="936b5-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="936b5-116">[**MCI \_ DGV \_ 保留 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="936b5-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936b5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="936b5-117">Return Value</span></span>

<span data-ttu-id="936b5-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="936b5-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="936b5-119">備註</span><span class="sxs-lookup"><span data-stu-id="936b5-119">Remarks</span></span>

<span data-ttu-id="936b5-120">如果工作區包含未儲存的資料，這項資料就會遺失。</span><span class="sxs-lookup"><span data-stu-id="936b5-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="936b5-121">如果在錄製之前未保留磁碟空間， [MCI \_ 記錄](mci-record.md) 命令會使用裝置特定的預設參數來執行隱含的保留。</span><span class="sxs-lookup"><span data-stu-id="936b5-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="936b5-122">在某些情況下，不需要保留，且可能會被設備磁碟機忽略。</span><span class="sxs-lookup"><span data-stu-id="936b5-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="936b5-123">明確保留空間可讓您更充分掌控磁片配置的延遲、配置的空間量，以及配置磁碟空間的位置。</span><span class="sxs-lookup"><span data-stu-id="936b5-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="936b5-124">您可以藉由再次發行 MCI 保留來變更已保留給此裝置實例的磁碟空間數量和位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="936b5-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="936b5-125">任何已配置且仍未使用的磁碟空間都不會解除配置，直到任何記錄的資料儲存或關閉設備磁碟機實例為止。</span><span class="sxs-lookup"><span data-stu-id="936b5-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="936b5-126">如果使用 \_ [mci \_ SETVIDEO](mci-setvideo.md) 命令的 mci off 旗標關閉影片，則保留的空間不會包含任何影片。</span><span class="sxs-lookup"><span data-stu-id="936b5-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="936b5-127">如果使用 \_ [mci \_ SETAUDIO](mci-setaudio.md) 命令的 mci off 旗標關閉音訊，則保留的空間不會包含任何音訊。</span><span class="sxs-lookup"><span data-stu-id="936b5-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="936b5-128">如果音訊和影片都已關閉，或者要求的大小為零，則不會保留任何空間，而且會解除配置任何現有的保留空間。</span><span class="sxs-lookup"><span data-stu-id="936b5-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="936b5-129">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="936b5-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="936b5-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI \_ DGV \_ 保留 \_</span><span class="sxs-lookup"><span data-stu-id="936b5-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="936b5-131">*LpReserve* 所識別之結構的 **lpstrPath** 成員包含包含暫存檔案位置的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="936b5-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="936b5-132">緩衝區只包含用來保存記錄資料之檔案的磁片磁碟機和目錄路徑;檔案名是由設備磁碟機所指定。</span><span class="sxs-lookup"><span data-stu-id="936b5-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="936b5-133">如果裝置實例已被明確儲存，則會刪除此暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="936b5-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="936b5-134">如果省略此旗標，設備磁碟機會指定磁碟空間的配置位置。</span><span class="sxs-lookup"><span data-stu-id="936b5-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="936b5-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI \_ DGV \_ 保留 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="936b5-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="936b5-136">*LpReserve* 所識別之結構的 **dwSize** 成員會指定要在工作區中保留的磁碟空間量，以進行錄製。</span><span class="sxs-lookup"><span data-stu-id="936b5-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="936b5-137">值是以目前時間格式指定。</span><span class="sxs-lookup"><span data-stu-id="936b5-137">The value is specified in the current time format.</span></span> <span data-ttu-id="936b5-138">磁碟空間的數量是從要求的時間，以及檔案格式和影片和音訊演算法和品質值的結果所估計。</span><span class="sxs-lookup"><span data-stu-id="936b5-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="936b5-139">如果省略此旗標，設備磁碟機可能會使用它所定義的預設值。</span><span class="sxs-lookup"><span data-stu-id="936b5-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="936b5-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="936b5-140">Requirements</span></span>



| <span data-ttu-id="936b5-141">需求</span><span class="sxs-lookup"><span data-stu-id="936b5-141">Requirement</span></span> | <span data-ttu-id="936b5-142">值</span><span class="sxs-lookup"><span data-stu-id="936b5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936b5-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="936b5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="936b5-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="936b5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="936b5-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="936b5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="936b5-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="936b5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="936b5-147">標頭</span><span class="sxs-lookup"><span data-stu-id="936b5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="936b5-148"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="936b5-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936b5-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="936b5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936b5-150">Mci</span><span class="sxs-lookup"><span data-stu-id="936b5-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="936b5-151">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="936b5-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

