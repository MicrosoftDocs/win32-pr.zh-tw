---
description: 為了防止未受限制的電話在電話語音系統中，如果無法識別應用程式是呼叫的初始擁有者，則 TAPI 會卸載從服務提供者發出的呼叫。
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: 未擁有的呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986371"
---
# <a name="unowned-calls"></a>未擁有的呼叫

為了防止未受限制的電話在電話語音系統中，如果無法識別應用程式是呼叫的初始擁有者，則 TAPI 會卸載從服務提供者發出的呼叫。 在 TAPI 2.0 版和更新版本中，TAPI 會呼叫 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) 函式來卸載呼叫。

服務提供者可以事先知道是否有應用程式可取得新呼叫的擁有權。 TAPI 一律會通知服務提供者可使用 [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) 函式提供應用程式的媒體類型。

例如，如果服務提供者判斷在具有 LINEMEDIAMODE INTERACTIVEVOICE 模式的行上有作用中的呼叫 \_ ，則應該先檢查預設媒體偵測，再產生 [**行 \_ NEWCALL**](line-newcall.md) 和 [**行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) 訊息。 如果預設的媒體偵測顯示沒有任何應用程式正在尋找 LINEMEDIAMODE \_ INTERACTIVEVOICE 呼叫，則服務提供者不應傳送訊息，因為 TAPI 會立即卸載訊息。

 

 
