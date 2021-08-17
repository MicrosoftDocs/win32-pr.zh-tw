---
title: 開啟裝置
description: 開啟裝置
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34408cef4e85ed7200b91c610e60ca546ff488ce5ad45edee12159a664f319fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802315"
---
# <a name="opening-a-device"></a>開啟裝置

使用裝置之前，您必須使用 [**open**](open.md) ([**MCI \_ open**](mci-open.md)) 命令將它初始化。 此命令會將驅動程式載入記憶體 (（如果尚未載入）) ，並在後續的 MCI 命令中抓取用來識別裝置的裝置識別碼。 您應該先檢查 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 或 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式的傳回值，再使用新的裝置識別碼，以確保識別碼有效。  (您也可以使用 [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) 函式來取得裝置識別碼。 ) 

就像所有的 MCI 命令訊息一樣， **\_ 開啟的 mci** 也有相關聯的結構。 這些結構有時也稱為 *參數區塊*。 **\_ 開啟的 mci** 預設結構是 [**mci \_ open \_ PARMS**](mci-open-parms.md)。 某些裝置 (例如 *波形**和重* 迭) 具有擴充結構 (例如 [**MCI \_ WAVE \_ open \_ PARMS**](mci-wave-open-parms.md)和 [**mci \_ OVLY \_ open \_ PARMS**](mci-ovly-open-parms.md)) 以容納其他選擇性參數。 除非您需要使用這些額外的參數，否則您可以將 **mci \_ OPEN \_ PARMS** 結構與任何 MCI 裝置搭配使用。

您可以開啟的裝置數目僅受限於可用記憶體的數量。

## <a name="using-an-alias"></a>使用別名

當您開啟裝置時，您可以使用「別名」旗標來指定裝置的裝置識別碼。 此旗標可讓您為具有冗長檔名的複合裝置指派簡短的裝置識別碼，並可讓您開啟相同檔案或裝置的多個實例。

例如，下列命令會將裝置識別碼 "birdcall" 指派給冗長的檔案名 C： \\ NABIRDS 音效 \\ \\ MOCKMTNG。WAV：


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



在命令訊息介面中，您可以使用 [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)結構的 **lpstrAlias** 成員來指定別名。

## <a name="specifying-a-device-type"></a>指定裝置類型

當您開啟裝置時，您可以使用「類型」旗標來參考裝置類型，而不是特定的設備磁碟機。 下列範例會開啟波形-音訊檔案 C： \\ WINDOWS \\ CHIMES。WAV (使用 "type" 旗標來指定 **waveaudio** 裝置類型) 並指派別名 "chimes"：


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



在命令訊息介面中，「類型」旗標的功能是由 [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)結構的 **lpstrDeviceType** 成員所提供。

## <a name="simple-and-compound-devices"></a>簡單和複合裝置

MCI 會將設備磁碟機分類為 *複合* 或 *簡單*。 複合裝置的驅動程式需要用來播放的資料檔案名稱;簡單裝置的驅動程式不會。

簡單的裝置包括 **cdaudio** 和 **videodisc** 裝置。 有兩種方式可以開啟簡單的裝置：

-   指定以 null 終止的字串指標，其中包含登錄或 SYSTEM.INI 檔案中的裝置名稱。

    例如，您可以使用下列命令來開啟 **videodisc** 裝置：


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



在此情況下，"videodisc" 是來自登錄或 SYSTEM.INI 的 mci 區段中的裝置名稱 \[ \] 。

-   指定設備磁碟機的實際名稱。 不過，使用裝置驅動程式檔案名來開啟裝置，會讓應用程式裝置特定，並可在系統組態變更時防止應用程式執行。 如果您使用檔案名，則不需要指定完整路徑或副檔名;MCI 假設驅動程式位於系統目錄中，並具有。WINSPOOL.DRV 副檔名。

複合裝置包括 **waveaudio** 和 **sequencer** 裝置。 複合裝置的資料有時稱為 *裝置元素*。 不過，這份檔通常會將此資料視為檔案，但在某些情況下，資料可能不會儲存為檔案。

有三種方式可以開啟複合裝置：

-   只指定裝置名稱。 這可讓您開啟複合裝置，而不需要建立檔案名的關聯。 大部分的複合裝置只會處理 ([**mci \_ GETDEVCAPS**](mci-getdevcaps.md)) 的 [**功能**](capability.md)，並在以這種方式開啟) 命令時 [**關閉**](close.md) ([**MCI \_**](mci-close.md) 。
-   僅指定檔案名。 裝置名稱是由登錄中的關聯所決定。
-   指定檔案名和裝置名稱。 MCI 會忽略登錄中的專案，並開啟指定的裝置名稱。

若要建立資料檔案與特定裝置的關聯，您可以指定檔案名和裝置名稱。 例如，下列命令會開啟具有檔案名 MYVOICE 的 **waveaudio** 裝置。SND：


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



在命令字串介面中，您也可以使用替代的驚嘆號格式來縮寫裝置名稱規格，如「 [**開啟**](open.md) 」命令所述。

## <a name="opening-a-device-using-the-filename-extension"></a>使用副檔名開啟裝置

如果 [**開啟**](open.md) 的 ([**MCI \_ 開啟**](mci-open.md)) 命令只指定檔案名，MCI 會使用副檔名從登錄中的清單或 SYSTEM.INI 檔的 [MCI 延伸模組] 區段中選取適當的裝置 \[ \] 。 [Mci 延伸模組] 區段中的專案 \[ \] 使用下列格式：

*\_ 副檔名*  =  *裝置 \_ 名稱*

如果找到擴充功能，且未在 **open** 命令中指定裝置名稱，則 MCI 會隱含地使用 *裝置 \_ 名稱*。

下列範例顯示一般的 \[ mci 擴充 \] 區段：


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



使用這些定義，如果發出下列命令，MCI 會開啟 **waveaudio** 裝置：


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>新的資料檔案

若要建立新的資料檔案，請只指定一個空白的檔案名。 在您使用 [ [**儲存**](save.md) ([**MCI \_ 儲存**](mci-save.md)) ] 命令儲存之前，MCI 不會儲存新檔案。 建立新檔案時，您必須包含具有 [**open**](open.md) ([**MCI \_ open**](mci-open.md)) 命令的裝置別名。

下列範例會開啟新的 **waveaudio** 檔案、啟動和停止錄製，然後儲存並關閉檔案：


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



## <a name="sharable-devices"></a>可共用的裝置

「可共用」 (MCI \_ 開啟 \_ [**開啟**](open.md) ([**MCI \_ open**](mci-open.md)) 命令的可共用) 旗標，可讓多個應用程式同時存取相同的裝置 (或檔案) 和裝置實例。 如果您的應用程式以可共用的方式開啟裝置或檔案，則其他應用程式也可以藉由開啟為可共用的方式來存取它。 共用的裝置或檔案讓每個應用程式都能夠變更控制其運作狀態的參數。 每次裝置或檔案開啟為可共用時，MCI 都會傳回唯一的裝置識別碼，即使識別碼參考相同的實例也是一樣。

如果您的應用程式開啟裝置或檔案，但未指定可共用它，則在您的應用程式關閉它之前，其他應用程式都無法存取它。 此外，如果裝置只支援一個開啟的實例，如果您指定可共用的旗標， **open** 命令將會失敗。

如果您的應用程式開啟裝置並指定可共用，則您的應用程式不應該對此裝置的狀態做出任何假設。 您的應用程式可能需要補償存取裝置的其他應用程式所做的變更。

大部分的複合檔案無法共用;不過，您可以開啟多個檔案，也可以多次開啟單一檔案。 如果您多次開啟單一檔案，MCI 會為每個檔案建立各自的獨立實例，每個實例都有唯一的運作狀態。

如果您開啟檔案的多個實例，則必須為每個實例指派唯一的裝置識別碼。 您可以使用別名（如下一節所述），為每個檔案指派唯一的名稱。

 

 