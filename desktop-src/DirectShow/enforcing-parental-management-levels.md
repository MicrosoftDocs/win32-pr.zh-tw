---
description: 強制執行家長管理層級
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: 強制執行家長管理層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467849"
---
# <a name="enforcing-parental-management-levels"></a>強制執行家長管理層級

DVD-Video 光碟上的任何標題或標題部分，都可以指派一般家長管理層級， (>PROCMONTRACE.PML) 從1到8。 當 DVD 導覽器讀取具有 >PROCMONTRACE.PML 的內容時，就表示它是在 *家長* 監護中。 家長監護可能包含章節、多個章節或多個標題的一部分。 適用于國際市場的 DVD 應用程式應該不會將特定評等系統硬編碼成其家長管理邏輯。

DVD 導覽器本身不會強制執行 PMLs;它只會在您的應用程式遇到光碟上的 >PROCMONTRACE.PML 資訊時通知您。根據預設，它會忽略光碟上的這項資訊，並播放最高層級的內容。 若要強制執行此 PMLs，您的應用程式必須執行某種形式的密碼控制邏輯，以將使用者與層級相關聯、指示 DVD 導覽器在啟動時呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) 方法來傳送 >procmontrace.pml 事件通知 (，並以 DVD \_ NotifyParentalLevelChange 和 **TRUE**) 參數來回應這些事件，以允許或不允許存取。

DVD 標題可以有一個整體 >PROCMONTRACE.PML，但光碟作者可以為該標題的某些區段提供較高或更嚴格的 PMLs。 這些稱為暫時性 >PROCMONTRACE.PML 命令;這些命令一律會包含兩個分支指示：當播放程式應用程式接受暫時性 >PROCMONTRACE.PML 命令時要遵循的指示，另一個則是在拒絕命令時遵循。 事件的順序如下所示。 當 (DVD 標題網域在光碟上遇到暫時性的 >PROCMONTRACE.PML 命令時，DVD 導覽程式會讀取該內容) 。它會檢查其內部旗標，以查看應用程式是否已要求收到此事件的通知。 如果未設定旗標，則會繼續播放 DVD，並遵循光碟上指定的「拒絕家長監護變更」分支。如果設定了旗標，DVD 會將 EC \_ DVD \_ 家長監護 \_ \_ 變更事件傳送至應用程式，並等待暫停狀態，直到收到回應為止。 當您的應用程式收到事件時，它會使用自己的邏輯來判斷是否要接受命令。 然後，它會使用 **TRUE** 或 **FALSE** 的引數來呼叫 [**IDvdControl2：： AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) 。 若 **為 TRUE**，則會在光碟上指定的「已接受家長監護變更」分支之後，繼續播放 DVD 導覽器。否則，它會繼續播放，並遵循「家長監護變更已拒絕」分支。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



