---
title: 應用程式復原和重新啟動
description: 撰寫自訂安裝程式，以自動重新開機已關機的應用程式以完成更新。 在結束程式之前，儲存資料並設定應用程式復原。
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- 可靠性
- 軟體可靠性
- 應用程式復原
- 應用程式重新開機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840687"
---
# <a name="application-recovery-and-restart"></a>應用程式復原和重新啟動

## <a name="purpose"></a>目的

應用程式可以使用應用程式復原，並重新啟動 (ARR) ，以在應用程式因未處理的例外狀況或應用程式停止回應之前結束之前儲存資料和狀態資訊。 如果要求，也會重新開機應用程式。

如果安裝程式更新應用程式的元件，或電腦需要重新開機做為更新的結果，也可以重新開機應用程式。 請注意，為了支援在安裝程式更新應用程式後自動重新開機應用程式，應用程式和安裝程式都需要適當撰寫。 如需詳細資訊，請參閱 [註冊應用程式重新開機](registering-for-application-restart.md)。

## <a name="developer-audience"></a>開發人員對象

ARR 是針對 C 和 c + + 開發人員所設計。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Vista 作業系統開始，可以使用 ARR。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                   | 描述                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [使用應用程式修復並重新啟動](using-application-recovery-and-restart.md)<br/>         | 註冊修復和重新開機的程式指南。<br/> |
| [應用程式修復和重新開機參考](application-recovery-and-restart-reference.md)<br/> | ARR API 的參考資訊。 <br/>                    |



 

 

 





