---
title: 開啟裝置
description: 開啟裝置
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023325"
---
# <a name="opening-a-device"></a><span data-ttu-id="98452-104">開啟裝置</span><span class="sxs-lookup"><span data-stu-id="98452-104">Opening a Device</span></span>

<span data-ttu-id="98452-105">使用裝置之前，您必須使用 [**open**](open.md) ([**MCI \_ open**](mci-open.md)) 命令將它初始化。</span><span class="sxs-lookup"><span data-stu-id="98452-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="98452-106">此命令會將驅動程式載入記憶體 (（如果尚未載入）) ，並在後續的 MCI 命令中抓取用來識別裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="98452-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="98452-107">您應該先檢查 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 或 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式的傳回值，再使用新的裝置識別碼，以確保識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="98452-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="98452-108"> (您也可以使用 [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) 函式來取得裝置識別碼。 ) </span><span class="sxs-lookup"><span data-stu-id="98452-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="98452-109">就像所有的 MCI 命令訊息一樣， **\_ 開啟的 mci** 也有相關聯的結構。</span><span class="sxs-lookup"><span data-stu-id="98452-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="98452-110">這些結構有時也稱為 *參數區塊*。</span><span class="sxs-lookup"><span data-stu-id="98452-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="98452-111">**\_ 開啟的 mci** 預設結構是 [**mci \_ open \_ PARMS**](mci-open-parms.md)。</span><span class="sxs-lookup"><span data-stu-id="98452-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="98452-112">某些裝置 (例如 *波形\*\*和重* 迭) 具有擴充結構 (例如 [**MCI \_ WAVE \_ open \_ PARMS**](mci-wave-open-parms.md)和 [**mci \_ OVLY \_ open \_ PARMS**](mci-ovly-open-parms.md)) 以容納其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="98452-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="98452-113">除非您需要使用這些額外的參數，否則您可以將 **mci \_ OPEN \_ PARMS** 結構與任何 MCI 裝置搭配使用。</span><span class="sxs-lookup"><span data-stu-id="98452-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="98452-114">您可以開啟的裝置數目僅受限於可用記憶體的數量。</span><span class="sxs-lookup"><span data-stu-id="98452-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="98452-115">使用別名</span><span class="sxs-lookup"><span data-stu-id="98452-115">Using an Alias</span></span>

<span data-ttu-id="98452-116">當您開啟裝置時，您可以使用「別名」旗標來指定裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="98452-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="98452-117">此旗標可讓您為具有冗長檔名的複合裝置指派簡短的裝置識別碼，並可讓您開啟相同檔案或裝置的多個實例。</span><span class="sxs-lookup"><span data-stu-id="98452-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="98452-118">例如，下列命令會將裝置識別碼 "birdcall" 指派給冗長的檔案名 C： \\ NABIRDS 音效 \\ \\ MOCKMTNG。Wav：</span><span class="sxs-lookup"><span data-stu-id="98452-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="98452-119">在命令訊息介面中，您可以使用 [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)結構的 **lpstrAlias** 成員來指定別名。</span><span class="sxs-lookup"><span data-stu-id="98452-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="98452-120">指定裝置類型</span><span class="sxs-lookup"><span data-stu-id="98452-120">Specifying a Device Type</span></span>

<span data-ttu-id="98452-121">當您開啟裝置時，您可以使用「類型」旗標來參考裝置類型，而不是特定的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="98452-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="98452-122">下列範例會開啟波形-音訊檔案 C： \\ WINDOWS \\ CHIMES。WAV (使用 "type" 旗標來指定 **waveaudio** 裝置類型) 並指派別名 "chimes"：</span><span class="sxs-lookup"><span data-stu-id="98452-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="98452-123">在命令訊息介面中，「類型」旗標的功能是由 [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)結構的 **lpstrDeviceType** 成員所提供。</span><span class="sxs-lookup"><span data-stu-id="98452-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="98452-124">簡單和複合裝置</span><span class="sxs-lookup"><span data-stu-id="98452-124">Simple and Compound Devices</span></span>

<span data-ttu-id="98452-125">MCI 會將設備磁碟機分類為 *複合* 或 *簡單*。</span><span class="sxs-lookup"><span data-stu-id="98452-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="98452-126">複合裝置的驅動程式需要用來播放的資料檔案名稱;簡單裝置的驅動程式不會。</span><span class="sxs-lookup"><span data-stu-id="98452-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="98452-127">簡單的裝置包括 **cdaudio** 和 **videodisc** 裝置。</span><span class="sxs-lookup"><span data-stu-id="98452-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="98452-128">有兩種方式可以開啟簡單的裝置：</span><span class="sxs-lookup"><span data-stu-id="98452-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="98452-129">指定以 null 終止的字串指標，其中包含登錄或 SYSTEM.INI 檔案中的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="98452-130">例如，您可以使用下列命令來開啟 **videodisc** 裝置：</span><span class="sxs-lookup"><span data-stu-id="98452-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="98452-131">在此情況下，"videodisc" 是來自登錄或 SYSTEM.INI 的 mci 區段中的裝置名稱 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="98452-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="98452-132">指定設備磁碟機的實際名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="98452-133">不過，使用裝置驅動程式檔案名來開啟裝置，會讓應用程式裝置特定，並可在系統組態變更時防止應用程式執行。</span><span class="sxs-lookup"><span data-stu-id="98452-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="98452-134">如果您使用檔案名，則不需要指定完整路徑或副檔名;MCI 假設驅動程式位於系統目錄中，並具有。WINSPOOL.DRV 副檔名。</span><span class="sxs-lookup"><span data-stu-id="98452-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="98452-135">複合裝置包括 **waveaudio** 和 **sequencer** 裝置。</span><span class="sxs-lookup"><span data-stu-id="98452-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="98452-136">複合裝置的資料有時稱為 *裝置元素*。</span><span class="sxs-lookup"><span data-stu-id="98452-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="98452-137">不過，這份檔通常會將此資料視為檔案，但在某些情況下，資料可能不會儲存為檔案。</span><span class="sxs-lookup"><span data-stu-id="98452-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="98452-138">有三種方式可以開啟複合裝置：</span><span class="sxs-lookup"><span data-stu-id="98452-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="98452-139">只指定裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-139">Specify only the device name.</span></span> <span data-ttu-id="98452-140">這可讓您開啟複合裝置，而不需要建立檔案名的關聯。</span><span class="sxs-lookup"><span data-stu-id="98452-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="98452-141">大部分的複合裝置只會處理 ([**mci \_ GETDEVCAPS**](mci-getdevcaps.md)) 的 [**功能**](capability.md)，並在以這種方式開啟) 命令時 [**關閉**](close.md) ([**MCI \_**](mci-close.md) 。</span><span class="sxs-lookup"><span data-stu-id="98452-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="98452-142">僅指定檔案名。</span><span class="sxs-lookup"><span data-stu-id="98452-142">Specify only the filename.</span></span> <span data-ttu-id="98452-143">裝置名稱是由登錄中的關聯所決定。</span><span class="sxs-lookup"><span data-stu-id="98452-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="98452-144">指定檔案名和裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-144">Specify the filename and the device name.</span></span> <span data-ttu-id="98452-145">MCI 會忽略登錄中的專案，並開啟指定的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="98452-146">若要建立資料檔案與特定裝置的關聯，您可以指定檔案名和裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="98452-147">例如，下列命令會開啟具有檔案名 MYVOICE 的 **waveaudio** 裝置。Snd：</span><span class="sxs-lookup"><span data-stu-id="98452-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="98452-148">在命令字串介面中，您也可以使用替代的驚嘆號格式來縮寫裝置名稱規格，如「 [**開啟**](open.md) 」命令所述。</span><span class="sxs-lookup"><span data-stu-id="98452-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="98452-149">使用副檔名開啟裝置</span><span class="sxs-lookup"><span data-stu-id="98452-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="98452-150">如果 [**開啟**](open.md) 的 ([**MCI \_ 開啟**](mci-open.md)) 命令只指定檔案名，MCI 會使用副檔名從登錄中的清單或 SYSTEM.INI 檔的 [MCI 延伸模組] 區段中選取適當的裝置 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="98452-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="98452-151">[Mci 延伸模組] 區段中的專案 \[ \] 使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="98452-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="98452-152">*\_ 副檔名*  =  *裝置 \_ 名稱*</span><span class="sxs-lookup"><span data-stu-id="98452-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="98452-153">如果找到擴充功能，且未在 **open** 命令中指定裝置名稱，則 MCI 會隱含地使用 *裝置 \_ 名稱*。</span><span class="sxs-lookup"><span data-stu-id="98452-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="98452-154">下列範例顯示一般的 \[ mci 擴充 \] 區段：</span><span class="sxs-lookup"><span data-stu-id="98452-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="98452-155">使用這些定義，如果發出下列命令，MCI 會開啟 **waveaudio** 裝置：</span><span class="sxs-lookup"><span data-stu-id="98452-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="98452-156">新的資料檔案</span><span class="sxs-lookup"><span data-stu-id="98452-156">New Data Files</span></span>

<span data-ttu-id="98452-157">若要建立新的資料檔案，請只指定一個空白的檔案名。</span><span class="sxs-lookup"><span data-stu-id="98452-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="98452-158">在您使用 [ [**儲存**](save.md) ([**MCI \_ 儲存**](mci-save.md)) ] 命令儲存之前，MCI 不會儲存新檔案。</span><span class="sxs-lookup"><span data-stu-id="98452-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="98452-159">建立新檔案時，您必須包含具有 [**open**](open.md) ([**MCI \_ open**](mci-open.md)) 命令的裝置別名。</span><span class="sxs-lookup"><span data-stu-id="98452-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="98452-160">下列範例會開啟新的 **waveaudio** 檔案、啟動和停止錄製，然後儲存並關閉檔案：</span><span class="sxs-lookup"><span data-stu-id="98452-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="98452-161">可共用的裝置</span><span class="sxs-lookup"><span data-stu-id="98452-161">Sharable Devices</span></span>

<span data-ttu-id="98452-162">「可共用」 (MCI \_ 開啟 \_ [**開啟**](open.md) ([**MCI \_ open**](mci-open.md)) 命令的可共用) 旗標，可讓多個應用程式同時存取相同的裝置 (或檔案) 和裝置實例。</span><span class="sxs-lookup"><span data-stu-id="98452-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="98452-163">如果您的應用程式以可共用的方式開啟裝置或檔案，則其他應用程式也可以藉由開啟為可共用的方式來存取它。</span><span class="sxs-lookup"><span data-stu-id="98452-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="98452-164">共用的裝置或檔案讓每個應用程式都能夠變更控制其運作狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="98452-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="98452-165">每次裝置或檔案開啟為可共用時，MCI 都會傳回唯一的裝置識別碼，即使識別碼參考相同的實例也是一樣。</span><span class="sxs-lookup"><span data-stu-id="98452-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="98452-166">如果您的應用程式開啟裝置或檔案，但未指定可共用它，則在您的應用程式關閉它之前，其他應用程式都無法存取它。</span><span class="sxs-lookup"><span data-stu-id="98452-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="98452-167">此外，如果裝置只支援一個開啟的實例，如果您指定可共用的旗標， **open** 命令將會失敗。</span><span class="sxs-lookup"><span data-stu-id="98452-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="98452-168">如果您的應用程式開啟裝置並指定可共用，則您的應用程式不應該對此裝置的狀態做出任何假設。</span><span class="sxs-lookup"><span data-stu-id="98452-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="98452-169">您的應用程式可能需要補償存取裝置的其他應用程式所做的變更。</span><span class="sxs-lookup"><span data-stu-id="98452-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="98452-170">大部分的複合檔案無法共用;不過，您可以開啟多個檔案，也可以多次開啟單一檔案。</span><span class="sxs-lookup"><span data-stu-id="98452-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="98452-171">如果您多次開啟單一檔案，MCI 會為每個檔案建立各自的獨立實例，每個實例都有唯一的運作狀態。</span><span class="sxs-lookup"><span data-stu-id="98452-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="98452-172">如果您開啟檔案的多個實例，則必須為每個實例指派唯一的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="98452-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="98452-173">您可以使用別名（如下一節所述），為每個檔案指派唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="98452-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 