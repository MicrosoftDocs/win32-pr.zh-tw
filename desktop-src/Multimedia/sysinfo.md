---
title: sysinfo 命令
description: Sysinfo 命令會抓取 MCI 系統資訊。 Sysinfo 命令是 MCI 系統命令;它是由 MCI 直接解讀。
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- sysinfo 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966347"
---
# <a name="sysinfo-command"></a><span data-ttu-id="77acd-105">sysinfo 命令</span><span class="sxs-lookup"><span data-stu-id="77acd-105">sysinfo command</span></span>

<span data-ttu-id="77acd-106">Sysinfo 命令會抓取 MCI 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="77acd-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="77acd-107">Sysinfo 命令是 MCI 系統命令;它是由 MCI 直接解讀。</span><span class="sxs-lookup"><span data-stu-id="77acd-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="77acd-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="77acd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="77acd-109">參數</span><span class="sxs-lookup"><span data-stu-id="77acd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77acd-110">*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="77acd-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="77acd-111">MCI 裝置或裝置類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="77acd-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="77acd-112">如果指定了裝置類型，則它必須是標準的 MCI 裝置類型名稱，如 [**功能**](capability.md) 命令的參考資料中所列。</span><span class="sxs-lookup"><span data-stu-id="77acd-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="77acd-113">您可以在 *lpszRequest* 中指定的旗標允許該可能性時，指定 "all"。</span><span class="sxs-lookup"><span data-stu-id="77acd-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="77acd-114">*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="77acd-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="77acd-115">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="77acd-115">One of the following flags.</span></span>



| <span data-ttu-id="77acd-116">值</span><span class="sxs-lookup"><span data-stu-id="77acd-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="77acd-117">意義</span><span class="sxs-lookup"><span data-stu-id="77acd-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="77acd-118"><dt>**installname**</dt></span><span class="sxs-lookup"><span data-stu-id="77acd-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="77acd-119">傳回登錄或 SYSTEM.INI 檔案中所列的名稱，用來安裝具有指定裝置識別碼的開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="77acd-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="77acd-120"><dt>**數量**</dt></span><span class="sxs-lookup"><span data-stu-id="77acd-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="77acd-121">傳回登錄中列出的 MCI 裝置數目或 *lpszDeviceID* 參數中指定之類型的 SYSTEM.INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="77acd-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="77acd-122">此裝置識別碼必須是標準的 MCI 裝置類型名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="77acd-123">裝置類型後的任何數位都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="77acd-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="77acd-124">針對 *lpszDeviceID* 指定 "all" 會傳回系統中的 MCI 裝置總數。</span><span class="sxs-lookup"><span data-stu-id="77acd-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="77acd-125"><dt>**已開啟數量**</dt></span><span class="sxs-lookup"><span data-stu-id="77acd-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="77acd-126">傳回 *lpszDeviceID* 中指定之類型的開啟 MCI 裝置數目。</span><span class="sxs-lookup"><span data-stu-id="77acd-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="77acd-127">此裝置識別碼必須是標準的 MCI 裝置類型名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="77acd-128">針對 *lpszDeviceID* 指定 "all" 會傳回系統中開啟的 MCI 裝置總數。</span><span class="sxs-lookup"><span data-stu-id="77acd-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="77acd-129"><dt>\* \* name \* index \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="77acd-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="77acd-130">傳回 MCI 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="77acd-131">裝置識別碼必須是標準的 MCI 裝置類型名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="77acd-132">*索引* 的範圍是從1到該類型的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="77acd-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="77acd-133">如果為 *lpszDeviceID* 指定 "all"， *索引* 的範圍會從1到系統中的裝置總數。</span><span class="sxs-lookup"><span data-stu-id="77acd-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="77acd-134"><dt>**名稱 *索引* 開啟**</dt></span><span class="sxs-lookup"><span data-stu-id="77acd-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="77acd-135">傳回開啟的 MCI 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="77acd-136">裝置識別碼必須是標準的 MCI 裝置類型名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="77acd-137">*索引* 的範圍是從1到該裝置類型的開啟裝置數目。</span><span class="sxs-lookup"><span data-stu-id="77acd-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="77acd-138">如果為 *lpszDeviceID* 指定 "all"， *索引* 的範圍會從1到系統中開啟的裝置總數。</span><span class="sxs-lookup"><span data-stu-id="77acd-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="77acd-139">*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="77acd-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="77acd-140">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="77acd-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="77acd-141">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="77acd-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="77acd-142">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="77acd-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="77acd-143">範例</span><span class="sxs-lookup"><span data-stu-id="77acd-143">Examples</span></span>

<span data-ttu-id="77acd-144">下列命令會傳回開啟的波形音訊裝置數目。</span><span class="sxs-lookup"><span data-stu-id="77acd-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="77acd-145">下列命令會傳回第一個開放式波形音訊裝置 (裝置別名) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="77acd-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="77acd-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="77acd-146">Requirements</span></span>



| <span data-ttu-id="77acd-147">需求</span><span class="sxs-lookup"><span data-stu-id="77acd-147">Requirement</span></span> | <span data-ttu-id="77acd-148">值</span><span class="sxs-lookup"><span data-stu-id="77acd-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="77acd-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77acd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="77acd-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77acd-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="77acd-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77acd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="77acd-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77acd-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="77acd-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77acd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77acd-154">Mci</span><span class="sxs-lookup"><span data-stu-id="77acd-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="77acd-155">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="77acd-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="77acd-156">**能力**</span><span class="sxs-lookup"><span data-stu-id="77acd-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

