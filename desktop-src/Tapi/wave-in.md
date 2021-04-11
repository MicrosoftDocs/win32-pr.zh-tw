---
description: Wave/in 裝置類別包含適用于低層級 wave 音訊輸入的音訊裝置。
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194494"
---
# <a name="wavein"></a><span data-ttu-id="9a376-103">wave/in</span><span class="sxs-lookup"><span data-stu-id="9a376-103">wave/in</span></span>

<span data-ttu-id="9a376-104">Wave/in 裝置類別包含適用于低層級 wave 音訊輸入的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="9a376-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="9a376-105">您可以使用 (SDK) 平臺軟體發展工具組中所述的 wave 功能來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="9a376-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="9a376-106">此類別中的裝置會與支援 LINEMEDIAMODE AUTOMATEDVOICE 媒體類型的線路裝置相關聯 \_ ，該媒體類型是線上路裝置之 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="9a376-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="9a376-107">[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="9a376-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="9a376-108">**DeviceId** 成員是封閉式音訊裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a376-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="9a376-109">在 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式的呼叫中，您可以使用此識別碼來開啟裝置以進行輸入。</span><span class="sxs-lookup"><span data-stu-id="9a376-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="9a376-110">您可以使用產生的裝置控制碼來記錄線路或電話裝置的數位化音訊資料。</span><span class="sxs-lookup"><span data-stu-id="9a376-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="9a376-111">雖然低層級 wave 音訊裝置也有「wave」裝置類別，但您應該一律針對低層級 wave 輸入使用 wave/in 裝置類別。</span><span class="sxs-lookup"><span data-stu-id="9a376-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="9a376-112">如需 wave 函數的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="9a376-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
