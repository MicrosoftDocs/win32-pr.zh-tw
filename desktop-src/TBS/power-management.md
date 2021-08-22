---
title: '電源管理 (TPM 基礎服務) '
description: TBS 會接收電源管理事件。
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece75e95065ca21d81ce7a3447cead33b6e3b8ae6693617fcb16bb27a30dd94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880692"
---
# <a name="power-management-tpm-base-services"></a>電源管理 (TPM 基礎服務) 

TBS 會接收電源管理事件。 當收到指示時，如果 TPM 或平臺的其他部分即將進入電源狀態，其中的執行將會中斷或 TPM 狀態將會遺失，則 TB 會檢查以判斷目前執行的命令是否可能在系統關機之前完成。 一般來說，TBS 允許 short 和 medium duration 命令完成，但會取消長時間的命令。 傳回命令之後，TBS 會停止將新的命令傳送至 TPM，並為休眠做好準備。 當電源恢復時，TBS 會將命令的結果傳回給呼叫者，然後繼續處理擱置中的 TBS 命令。 TBS 電源管理程式碼會以非同步方式執行，因此即使 TPM 正在處理長命令，也可以處理電源管理要求。

當電腦進入睡眠狀態時，包括 S3 (睡眠) 和 S4 (休眠) 時，TPM 會關閉電源。 因此，所有非持續性 TPM 狀態都會遺失。 進入這些狀態之前，應用程式軟體應該準備好遺失暫時性 TPM 狀態。 當系統從睡眠狀態恢復時，會與 TPM 進行同步處理，讓 [TB] 狀態與 TPM 狀態一致。 應用程式軟體可能需要重新發出中斷的命令。

 

 




