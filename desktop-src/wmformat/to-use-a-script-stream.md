---
title: 使用腳本資料流程
description: 使用腳本資料流程
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK，腳本資料流程
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- 腳本資料流程，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444729"
---
# <a name="to-use-a-script-stream"></a>使用腳本資料流程

本節說明如何將腳本資料傳送至寫入器，以便包含在檔案中。 如需在設定檔中包含腳本資料流程的詳細資訊，請參閱設定 [任意資料流程類型](configuring-arbitrary-stream-types.md)。

每個腳本都包含兩個字串： *類型* 字串和 *引數* 字串。

腳本資料必須先格式化，才能傳送到寫入器。 字串應串連，並以 **null** 字元分隔，並以 **null** 字元結束。 下列範例顯示合法的腳本：



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | &nbsp; | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | &nbsp; |



 

每一對指令碼命令都應該撰寫為寫入器的範例。 如需撰寫範例的詳細資訊，請參閱 [撰寫範例](to-write-samples.md)。

當您播放 ASF 檔案時，讀取器 (或同步讀取器會將指令碼命令傳遞至展示時間順序中) 。 應用程式必須負責剖析兩個字串，並回應指令碼命令。

> [!Note]  
> 使用 DRM 加密檔案時，沒有指令碼命令可以有0的呈現時間。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用指令碼命令**](using-script-commands.md)
</dt> </dl>

 

 




