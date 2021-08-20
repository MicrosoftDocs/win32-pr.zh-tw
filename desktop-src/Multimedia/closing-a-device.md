---
title: 關閉裝置
description: 關閉裝置
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f81ddaf42ef5509b55271159b8e36ac56584b92734a6b04e5b555041596530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498078"
---
# <a name="closing-a-device"></a>關閉裝置

[**Close**](close.md) ([**MCI \_ close**](mci-close.md)) 命令會釋放對裝置或檔案的存取權。 當使用裝置的所有工作都已關閉時，MCI 會釋出裝置。 若要協助 MCI 管理裝置，您的應用程式必須在使用完畢後關閉每個裝置或檔案。

當您關閉的外部 MCI 裝置使用自己的媒體，而不是檔案 (例如 CD 音訊) 時，驅動程式會將裝置保持在目前的作業模式中。 因此，如果您關閉現正播放的 CD 音訊裝置，即使設備磁碟機是從記憶體釋放，CD 音訊裝置仍會繼續播放，直到到達其內容的結尾為止。

> [!Note]  
> 使用開啟的 MCI 裝置關閉應用程式，可以防止其他應用程式使用這些裝置，直到 Windows 重新開機為止。

 

 

 




