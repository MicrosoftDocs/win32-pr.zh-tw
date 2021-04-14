---
title: 關閉裝置
description: 關閉裝置
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371890"
---
# <a name="closing-a-device"></a><span data-ttu-id="bbd85-104">關閉裝置</span><span class="sxs-lookup"><span data-stu-id="bbd85-104">Closing a Device</span></span>

<span data-ttu-id="bbd85-105">[**Close**](close.md) ([**MCI \_ close**](mci-close.md)) 命令會釋放對裝置或檔案的存取權。</span><span class="sxs-lookup"><span data-stu-id="bbd85-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="bbd85-106">當使用裝置的所有工作都已關閉時，MCI 會釋出裝置。</span><span class="sxs-lookup"><span data-stu-id="bbd85-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="bbd85-107">若要協助 MCI 管理裝置，您的應用程式必須在使用完畢後關閉每個裝置或檔案。</span><span class="sxs-lookup"><span data-stu-id="bbd85-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="bbd85-108">當您關閉的外部 MCI 裝置使用自己的媒體，而不是檔案 (例如 CD 音訊) 時，驅動程式會將裝置保持在目前的作業模式中。</span><span class="sxs-lookup"><span data-stu-id="bbd85-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="bbd85-109">因此，如果您關閉現正播放的 CD 音訊裝置，即使設備磁碟機是從記憶體釋放，CD 音訊裝置仍會繼續播放，直到到達其內容的結尾為止。</span><span class="sxs-lookup"><span data-stu-id="bbd85-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="bbd85-110">使用開啟的 MCI 裝置關閉應用程式，可以防止其他應用程式使用這些裝置，直到重新開機 Windows 為止。</span><span class="sxs-lookup"><span data-stu-id="bbd85-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




