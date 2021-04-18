---
title: 'MCI_LIST 命令 (Mmsystem .h) '
description: MCI \_ 清單命令可取得裝置可用輸入的數目和類型的相關資訊。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509415"
---
# <a name="mci_list-command"></a><span data-ttu-id="35fc8-105">MCI \_ 清單命令</span><span class="sxs-lookup"><span data-stu-id="35fc8-105">MCI\_LIST command</span></span>

<span data-ttu-id="35fc8-106">MCI \_ 清單命令可取得裝置可用輸入的數目和類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="35fc8-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="35fc8-107">數位影片和 VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="35fc8-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="35fc8-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="35fc8-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="35fc8-109">參數</span><span class="sxs-lookup"><span data-stu-id="35fc8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fc8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="35fc8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="35fc8-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="35fc8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="35fc8-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="35fc8-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="35fc8-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span><span class="sxs-lookup"><span data-stu-id="35fc8-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="35fc8-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="35fc8-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="35fc8-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fc8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="35fc8-118">Return Value</span></span>

<span data-ttu-id="35fc8-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="35fc8-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="35fc8-120">備註</span><span class="sxs-lookup"><span data-stu-id="35fc8-120">Remarks</span></span>

<span data-ttu-id="35fc8-121">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="35fc8-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="35fc8-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ 清單 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="35fc8-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-123">*LpList* 所識別之結構的 **lpstrAlgorithm** 成員包含包含演算法名稱之緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="35fc8-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="35fc8-124">此名稱會用來抓取與演算法相關聯的品質描述項類型。</span><span class="sxs-lookup"><span data-stu-id="35fc8-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI \_ DGV \_ 清單 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="35fc8-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-126">傳回指定類型的選項數目。</span><span class="sxs-lookup"><span data-stu-id="35fc8-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI \_ DGV \_ 清單 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="35fc8-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-128">常數，表示清單類型包含在 *lpList* 所識別之結構的 **dwItem** 成員中。</span><span class="sxs-lookup"><span data-stu-id="35fc8-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="35fc8-129">此為必要旗標。</span><span class="sxs-lookup"><span data-stu-id="35fc8-129">This flag is required.</span></span> <span data-ttu-id="35fc8-130">您可以使用下列其中一個常數來表示清單類型：</span><span class="sxs-lookup"><span data-stu-id="35fc8-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ 列出 \_ 音訊 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="35fc8-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-132">此命令應該會取出音訊演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="35fc8-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ 列出 \_ 音訊 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="35fc8-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-134">此命令應該會取出音訊品質層級。</span><span class="sxs-lookup"><span data-stu-id="35fc8-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="35fc8-135">傳回的層級與 *lpList* 所識別之結構的 **lpstrAlgorithm** 成員所參考的演算法相關聯。</span><span class="sxs-lookup"><span data-stu-id="35fc8-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="35fc8-136">如果使用字串 "current" 指定該成員，則會傳回與目前演算法相關聯的品質。</span><span class="sxs-lookup"><span data-stu-id="35fc8-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI \_ DGV \_ 列出 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="35fc8-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-138">此命令應該會取出音訊串流的名稱。</span><span class="sxs-lookup"><span data-stu-id="35fc8-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI \_ DGV \_ 清單 \_ 仍在 \_ AL</span><span class="sxs-lookup"><span data-stu-id="35fc8-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-140">此命令應該會取出仍為演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="35fc8-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI \_ DGV \_ 清單 \_ 仍為 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="35fc8-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-142">此命令應該會取出品質層級。</span><span class="sxs-lookup"><span data-stu-id="35fc8-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="35fc8-143">傳回的層級與 *lpList* 所識別之結構的 **lpstrAlgorithm** 成員所參考的演算法相關聯。</span><span class="sxs-lookup"><span data-stu-id="35fc8-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="35fc8-144">如果使用字串 "current" 指定該成員，則會傳回與目前演算法相關聯的品質。</span><span class="sxs-lookup"><span data-stu-id="35fc8-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ ALG</span><span class="sxs-lookup"><span data-stu-id="35fc8-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-146">此命令應該會取出影片演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="35fc8-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="35fc8-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-148">此命令應該會取出影片品質層級。</span><span class="sxs-lookup"><span data-stu-id="35fc8-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="35fc8-149">傳回的層級與 *lpList* 所識別之結構的 **lpstrAlgorithm** 成員所參考的演算法相關聯。</span><span class="sxs-lookup"><span data-stu-id="35fc8-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="35fc8-150">如果使用字串 "current" 指定該成員，則會傳回與目前演算法相關聯的品質。</span><span class="sxs-lookup"><span data-stu-id="35fc8-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="35fc8-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-152">此命令應該會傳回影片來源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="35fc8-152">The command should return information about the video sources.</span></span> <span data-ttu-id="35fc8-153">搭配 MCI \_ DGV \_ LIST COUNT 使用時 \_ ，此命令會傳回影片來源的數目。</span><span class="sxs-lookup"><span data-stu-id="35fc8-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="35fc8-154">搭配 MCI \_ DGV \_ LIST NUMBER 使用時 \_ ，此命令會傳回影片來源的類型。</span><span class="sxs-lookup"><span data-stu-id="35fc8-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="35fc8-155">MCI 定義了下列類型：</span><span class="sxs-lookup"><span data-stu-id="35fc8-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="35fc8-156">MCI \_ DGV \_ SETVIDEO \_ SRC \_ GENERIC</span><span class="sxs-lookup"><span data-stu-id="35fc8-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="35fc8-157">MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC</span><span class="sxs-lookup"><span data-stu-id="35fc8-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="35fc8-158">MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL</span><span class="sxs-lookup"><span data-stu-id="35fc8-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="35fc8-159">MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB</span><span class="sxs-lookup"><span data-stu-id="35fc8-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="35fc8-160">MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM</span><span class="sxs-lookup"><span data-stu-id="35fc8-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="35fc8-161">MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO</span><span class="sxs-lookup"><span data-stu-id="35fc8-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="35fc8-162">傳回的每個類型可能會有一個以上的來源。</span><span class="sxs-lookup"><span data-stu-id="35fc8-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="35fc8-163">當該連接器允許一個以上的信號類型時，就會使用泛型來源類型。</span><span class="sxs-lookup"><span data-stu-id="35fc8-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="35fc8-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-165">此命令應該會取出視頻資料流程的名稱。</span><span class="sxs-lookup"><span data-stu-id="35fc8-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI \_ DGV \_ 清單 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="35fc8-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-167">在 *lpList* 所識別之結構的 **dwNumber** 成員中指定索引。</span><span class="sxs-lookup"><span data-stu-id="35fc8-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="35fc8-168">索引必須是介於1和針對 MCI \_ DGV \_ LIST COUNT 旗標傳回值之間的整數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35fc8-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="35fc8-169">針對數位影片裝置， *lpList* 會指向 [**MCI \_ DGV \_ 清單 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="35fc8-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="35fc8-170">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="35fc8-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="35fc8-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI \_ VCR \_ 清單 \_ 音訊 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="35fc8-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-172">列出音訊輸入或類型。</span><span class="sxs-lookup"><span data-stu-id="35fc8-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI \_ VCR \_ 清單 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="35fc8-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-174">將 *lpList* 所識別之結構的 **dwReturn** 成員設定為影片或音訊輸入的總數目。</span><span class="sxs-lookup"><span data-stu-id="35fc8-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI \_ VCR \_ 清單 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="35fc8-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-176">將 *lpList* 所識別之結構的 **dwReturn** 成員設定為 **dwNumber** 成員所指定之影片或音訊輸入的類型。</span><span class="sxs-lookup"><span data-stu-id="35fc8-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="35fc8-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI \_ VCR \_ 清單 \_ 影片 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="35fc8-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="35fc8-178">列出影片輸入或類型。</span><span class="sxs-lookup"><span data-stu-id="35fc8-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="35fc8-179">若為 VCR 裝置， *lpList* 會指向 [**MCI \_ VCR \_ 清單 \_ PARMS**](mci-vcr-list-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="35fc8-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fc8-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="35fc8-180">Requirements</span></span>



| <span data-ttu-id="35fc8-181">需求</span><span class="sxs-lookup"><span data-stu-id="35fc8-181">Requirement</span></span> | <span data-ttu-id="35fc8-182">值</span><span class="sxs-lookup"><span data-stu-id="35fc8-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fc8-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35fc8-183">Minimum supported client</span></span><br/> | <span data-ttu-id="35fc8-184">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35fc8-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="35fc8-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35fc8-185">Minimum supported server</span></span><br/> | <span data-ttu-id="35fc8-186">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35fc8-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="35fc8-187">標頭</span><span class="sxs-lookup"><span data-stu-id="35fc8-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fc8-188"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="35fc8-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fc8-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35fc8-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fc8-190">Mci</span><span class="sxs-lookup"><span data-stu-id="35fc8-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="35fc8-191">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="35fc8-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

