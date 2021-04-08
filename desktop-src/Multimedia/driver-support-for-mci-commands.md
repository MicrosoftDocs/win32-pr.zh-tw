---
title: MCI 命令的驅動程式支援
description: MCI 命令的驅動程式支援
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672591"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="ecfdf-103">MCI 命令的驅動程式支援</span><span class="sxs-lookup"><span data-stu-id="ecfdf-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="ecfdf-104">MCI 驅動程式提供 MCI 命令的功能。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="ecfdf-105">系統軟體會執行一些基本的資料管理工作，但是所有的多媒體播放、簡報和錄製都是由個別的 MCI 驅動程式來處理。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="ecfdf-106">驅動程式在其支援 MCI 命令和命令旗標方面各有不同。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="ecfdf-107">由於多媒體裝置有很大的不同功能，因此 MCI 的設計目的是要讓個別的驅動程式擴充或縮減命令集，以符合裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="ecfdf-108">例如， [**記錄**](record.md) ([**MCI \_ 記錄**](mci-record.md)) 命令是適用于 MIDI sequencers 的命令集的一部分，但是 Windows 隨附的 MCISEQ 驅動程式不支援此命令。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="ecfdf-109">[記錄] 命令的參考主題說明 **sequencer** 裝置類型的裝置可辨識命令;這並不表示此類型的所有裝置都支援該命令。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="ecfdf-110">應用程式應該使用 ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) 命令的 [**功能**](capability.md)來判斷特定裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="ecfdf-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




