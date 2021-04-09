---
description: Midi/in 裝置類別包含用於輸入的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689447"
---
# <a name="midiin"></a><span data-ttu-id="446c0-104">midi/in</span><span class="sxs-lookup"><span data-stu-id="446c0-104">midi/in</span></span>

<span data-ttu-id="446c0-105">Midi/in 裝置類別包含用於輸入的 MIDI sequencers。</span><span class="sxs-lookup"><span data-stu-id="446c0-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="446c0-106">您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="446c0-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="446c0-107">[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="446c0-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="446c0-108">**DeviceId** 成員是封閉式 MIDI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="446c0-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="446c0-109">在 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式的呼叫中，您可以使用此識別碼來開啟裝置以進行輸入。</span><span class="sxs-lookup"><span data-stu-id="446c0-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="446c0-110">您可以使用產生的裝置控制碼，從線路或電話裝置錄製 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="446c0-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="446c0-111">如需有關 MIDI 功能的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="446c0-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
