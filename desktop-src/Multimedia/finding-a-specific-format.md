---
title: 尋找特定格式
description: 尋找特定格式
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- 音訊壓縮管理員 (的) ，尋找格式
- " (音效壓縮管理員) 、尋找格式"
- 進行中的範例，尋找格式
- 尋找格式
- acmFormatEnum 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc291a6dff0c6b2befec6afd001a32735a54e95fd65a464378adb690a95019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691528"
---
# <a name="finding-a-specific-format"></a>尋找特定格式

當應用程式需要完整規格時，可能只會有格式的部分規格。 例如，規格可能會規定 11-kHz mono、4位 ADPCM 格式，但不能是每秒的平均位元組數。 應用程式可以在不需要使用者介入的情況下取得完整格式，方法是使用 [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) 函式，並在 *fdwEnum* 參數中指定旗標。

 

 




