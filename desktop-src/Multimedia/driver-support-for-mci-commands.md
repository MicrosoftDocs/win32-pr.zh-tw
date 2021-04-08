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
# <a name="driver-support-for-mci-commands"></a>MCI 命令的驅動程式支援

MCI 驅動程式提供 MCI 命令的功能。 系統軟體會執行一些基本的資料管理工作，但是所有的多媒體播放、簡報和錄製都是由個別的 MCI 驅動程式來處理。

驅動程式在其支援 MCI 命令和命令旗標方面各有不同。 由於多媒體裝置有很大的不同功能，因此 MCI 的設計目的是要讓個別的驅動程式擴充或縮減命令集，以符合裝置的功能。 例如， [**記錄**](record.md) ([**MCI \_ 記錄**](mci-record.md)) 命令是適用于 MIDI sequencers 的命令集的一部分，但是 Windows 隨附的 MCISEQ 驅動程式不支援此命令。 [記錄] 命令的參考主題說明 **sequencer** 裝置類型的裝置可辨識命令;這並不表示此類型的所有裝置都支援該命令。 應用程式應該使用 ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) 命令的 [**功能**](capability.md)來判斷特定裝置的功能。

 

 




