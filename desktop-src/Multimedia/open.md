---
title: '開啟命令 (Corecrt \_) '
description: Open 命令會初始化裝置。 所有 MCI 裝置都會辨識此命令。
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- 開啟命令 Windows 多媒體
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685890"
---
# <a name="open-command"></a><span data-ttu-id="af447-105">開啟命令</span><span class="sxs-lookup"><span data-stu-id="af447-105">open command</span></span>

<span data-ttu-id="af447-106">Open 命令會初始化裝置。</span><span class="sxs-lookup"><span data-stu-id="af447-106">The open command initializes a device.</span></span> <span data-ttu-id="af447-107">所有 MCI 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="af447-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="af447-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="af447-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="af447-109">參數</span><span class="sxs-lookup"><span data-stu-id="af447-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af447-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span><span class="sxs-lookup"><span data-stu-id="af447-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="af447-111">MCI 裝置或設備磁碟機的識別碼。</span><span class="sxs-lookup"><span data-stu-id="af447-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="af447-112">這可以是在登錄中指定的裝置名稱 (或 SYSTEM.INI 檔) 或設備磁碟機的檔案名。</span><span class="sxs-lookup"><span data-stu-id="af447-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="af447-113">如果您指定設備磁碟機的檔案名，則可以選擇性地包含。WINSPOOL.DRV 延伸模組，但您不應該包含檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="af447-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="af447-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span><span class="sxs-lookup"><span data-stu-id="af447-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="af447-115">識別要初始化之內容的旗標。</span><span class="sxs-lookup"><span data-stu-id="af447-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="af447-116">下表列出可辨識 **開啟** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="af447-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="af447-117">值</span><span class="sxs-lookup"><span data-stu-id="af447-117">Value</span></span>        | <span data-ttu-id="af447-118">意義</span><span class="sxs-lookup"><span data-stu-id="af447-118">Meaning</span></span>                                                        | <span data-ttu-id="af447-119">意義</span><span class="sxs-lookup"><span data-stu-id="af447-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="af447-120">cdaudio</span><span class="sxs-lookup"><span data-stu-id="af447-120">cdaudio</span></span>      | <span data-ttu-id="af447-121">別名 *裝置 \_ 別名* 可共用</span><span class="sxs-lookup"><span data-stu-id="af447-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="af447-122">類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="af447-123">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="af447-123">digitalvideo</span></span> | <span data-ttu-id="af447-124">別名 *裝置 \_ aliaselementname* nostatic 父 *hwnd* 可共用</span><span class="sxs-lookup"><span data-stu-id="af447-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="af447-125">樣式子樣式重迭樣式的快顯樣式 *樣式 \_ 類型* 類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="af447-126">overlay</span><span class="sxs-lookup"><span data-stu-id="af447-126">overlay</span></span>      | <span data-ttu-id="af447-127">別名 *裝置 \_ 別名* 父系 *hwnd* 可共用樣式子系</span><span class="sxs-lookup"><span data-stu-id="af447-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="af447-128">樣式重迭樣式的快顯樣式 *樣式 \_ 類型* 類型 *裝置 \_* 類型</span><span class="sxs-lookup"><span data-stu-id="af447-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="af447-129">排序器</span><span class="sxs-lookup"><span data-stu-id="af447-129">sequencer</span></span>    | <span data-ttu-id="af447-130">別名 *裝置 \_ 別名* 可共用</span><span class="sxs-lookup"><span data-stu-id="af447-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="af447-131">類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="af447-132">錄影機</span><span class="sxs-lookup"><span data-stu-id="af447-132">vcr</span></span>          | <span data-ttu-id="af447-133">別名 *裝置 \_ 別名* 可共用</span><span class="sxs-lookup"><span data-stu-id="af447-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="af447-134">類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="af447-135">videodisk</span><span class="sxs-lookup"><span data-stu-id="af447-135">videodisk</span></span>    | <span data-ttu-id="af447-136">別名 *裝置 \_ 別名* 可共用</span><span class="sxs-lookup"><span data-stu-id="af447-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="af447-137">類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="af447-138">waveaudio</span><span class="sxs-lookup"><span data-stu-id="af447-138">waveaudio</span></span>    | <span data-ttu-id="af447-139">別名 *裝置 \_ 別名* 緩衝區 *緩衝區 \_ 大小*</span><span class="sxs-lookup"><span data-stu-id="af447-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="af447-140">可共用的類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="af447-141">下表列出可在 **lpszOpenFlags** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="af447-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="af447-142">值</span><span class="sxs-lookup"><span data-stu-id="af447-142">Value</span></span>                 | <span data-ttu-id="af447-143">意義</span><span class="sxs-lookup"><span data-stu-id="af447-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af447-144">別名 *裝置 \_ 別名*</span><span class="sxs-lookup"><span data-stu-id="af447-144">alias *device\_alias*</span></span> | <span data-ttu-id="af447-145">指定指定裝置的替代名稱。</span><span class="sxs-lookup"><span data-stu-id="af447-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="af447-146">如果有指定，就必須在後續命令中用來作為 *裝置 \_ 識別碼* 。</span><span class="sxs-lookup"><span data-stu-id="af447-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="af447-147">*elementname*</span><span class="sxs-lookup"><span data-stu-id="af447-147">*elementname*</span></span>         | <span data-ttu-id="af447-148">指定裝置在裝置開啟時載入 (檔的名稱) 。</span><span class="sxs-lookup"><span data-stu-id="af447-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="af447-149">緩衝區 *緩衝區 \_ 大小*</span><span class="sxs-lookup"><span data-stu-id="af447-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="af447-150">設定波形音訊裝置所使用之緩衝區的大小（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="af447-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="af447-151">安裝或設定波形音訊裝置時，會設定緩衝區的預設大小。</span><span class="sxs-lookup"><span data-stu-id="af447-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="af447-152">緩衝區大小通常會設定為4秒。</span><span class="sxs-lookup"><span data-stu-id="af447-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="af447-153">使用 MCIWAVE 裝置時，大小下限為2秒，而大小上限為9秒。</span><span class="sxs-lookup"><span data-stu-id="af447-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="af447-154">父 *hwnd*</span><span class="sxs-lookup"><span data-stu-id="af447-154">parent *hwnd*</span></span>         | <span data-ttu-id="af447-155">指定父視窗的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="af447-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="af447-156">共用</span><span class="sxs-lookup"><span data-stu-id="af447-156">sharable</span></span>              | <span data-ttu-id="af447-157">將裝置或檔案初始化為可共用。</span><span class="sxs-lookup"><span data-stu-id="af447-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="af447-158">除非您在原始和後續的 **開啟** 命令中指定「可共用」，否則後續開啟裝置或檔案的嘗試都會失敗。</span><span class="sxs-lookup"><span data-stu-id="af447-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="af447-159">如果裝置已開啟且無法共用，則 MCI 會傳回不正確裝置錯誤。</span><span class="sxs-lookup"><span data-stu-id="af447-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="af447-160">MCISEQ sequencer 和 MCIWAVE 裝置不支援共用檔案。</span><span class="sxs-lookup"><span data-stu-id="af447-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="af447-161">樣式子系</span><span class="sxs-lookup"><span data-stu-id="af447-161">style child</span></span>           | <span data-ttu-id="af447-162">開啟具有子視窗樣式的視窗。</span><span class="sxs-lookup"><span data-stu-id="af447-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="af447-163">樣式重迭</span><span class="sxs-lookup"><span data-stu-id="af447-163">style overlapped</span></span>      | <span data-ttu-id="af447-164">開啟具有重迭視窗樣式的視窗。</span><span class="sxs-lookup"><span data-stu-id="af447-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="af447-165">樣式快顯視窗</span><span class="sxs-lookup"><span data-stu-id="af447-165">style popup</span></span>           | <span data-ttu-id="af447-166">以快顯視窗樣式開啟視窗。</span><span class="sxs-lookup"><span data-stu-id="af447-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="af447-167">樣式 *樣式 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-167">style *style\_type*</span></span>   | <span data-ttu-id="af447-168">表示視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="af447-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="af447-169">類型 *裝置 \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="af447-169">type *device\_type*</span></span>   | <span data-ttu-id="af447-170">指定檔案的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="af447-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="af447-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="af447-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="af447-172">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="af447-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="af447-173">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="af447-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af447-174">傳回值</span><span class="sxs-lookup"><span data-stu-id="af447-174">Return Value</span></span>

<span data-ttu-id="af447-175">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="af447-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af447-176">備註</span><span class="sxs-lookup"><span data-stu-id="af447-176">Remarks</span></span>

<span data-ttu-id="af447-177">MCI 會針對 CD 音訊裝置類型、"videodisc" （適用于 videodisc 裝置類型）、"sequencer" （適用于 MIDI sequencer 裝置類型）、"AVIVideo" （適用于數位視訊裝置類型）和 "waveaudio" （波形音訊裝置類型）保留 "cdaudio"。</span><span class="sxs-lookup"><span data-stu-id="af447-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="af447-178">除了「類型」旗標以外，MCI 也可以根據檔案所使用的擴充功能來選取裝置，如登錄或 SYSTEM.INI 檔案的 \[ MCI 延伸區段中所記錄 \] 。</span><span class="sxs-lookup"><span data-stu-id="af447-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="af447-179">MCI 可以使用檔案介面指標或資料流程介面指標來開啟 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="af447-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="af447-180">若要使用任一種類型的介面指標來開啟檔案，請指定 @ 符號 ( @ ) 後面接著介面指標，以取代 *lpszDevice* 參數的檔案或裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="af447-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="af447-181">如需檔案和資料流程介面的詳細資訊，請參閱「AVIFile 函式 [和宏](avifile-functions-and-macros.md)」。</span><span class="sxs-lookup"><span data-stu-id="af447-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="af447-182">下列命令會開啟 "mysound" 裝置。</span><span class="sxs-lookup"><span data-stu-id="af447-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="af447-183">使用裝置名稱 "new" 時，波形驅動程式會準備新的波形資源。</span><span class="sxs-lookup"><span data-stu-id="af447-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="af447-184">此命令會指派裝置別名 "mysound"，並指定6秒的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="af447-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="af447-185">如果您將裝置名稱與檔案名結合，則可以消除「類型」旗標。</span><span class="sxs-lookup"><span data-stu-id="af447-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="af447-186">當您使用下列語法時，MCI 會辨識此組合：</span><span class="sxs-lookup"><span data-stu-id="af447-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="af447-187">*裝置 \_ 名稱* ！</span><span class="sxs-lookup"><span data-stu-id="af447-187">*device\_name* !</span></span> <span data-ttu-id="af447-188">*元素 \_ 名稱*</span><span class="sxs-lookup"><span data-stu-id="af447-188">*element\_name*</span></span>

<span data-ttu-id="af447-189">驚嘆號會將裝置名稱與檔案名分隔開來。</span><span class="sxs-lookup"><span data-stu-id="af447-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="af447-190">驚嘆號不應以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="af447-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="af447-191">下列範例會開啟右邊。使用 "waveaudio" 裝置的 WAV 檔案。</span><span class="sxs-lookup"><span data-stu-id="af447-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="af447-192">MCIWAVE 驅動程式需要非同步波形音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="af447-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="af447-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="af447-193">Requirements</span></span>



| <span data-ttu-id="af447-194">需求</span><span class="sxs-lookup"><span data-stu-id="af447-194">Requirement</span></span> | <span data-ttu-id="af447-195">值</span><span class="sxs-lookup"><span data-stu-id="af447-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af447-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af447-196">Minimum supported client</span></span><br/> | <span data-ttu-id="af447-197">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af447-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="af447-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af447-198">Minimum supported server</span></span><br/> | <span data-ttu-id="af447-199">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af447-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="af447-200">標頭</span><span class="sxs-lookup"><span data-stu-id="af447-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="af447-201"><dt>Corecrt \_ 的 io。h</dt></span><span class="sxs-lookup"><span data-stu-id="af447-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af447-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af447-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af447-203">Mci</span><span class="sxs-lookup"><span data-stu-id="af447-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="af447-204">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="af447-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

