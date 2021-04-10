---
title: 建立具有多個會話的光碟
description: IMAPI.EXE 能夠建立多會話資料光碟。 建立多會話光碟時，有幾個需要注意的事項。
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183345"
---
# <a name="creating-discs-with-multiple-sessions"></a>建立具有多個會話的光碟

IMAPI.EXE 能夠建立多會話資料光碟。 建立多會話光碟時，有幾個需要注意的事項。

[**IDiscMaster：： SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder)方法會判斷在設定時是否有使用中磁片磁碟機的 imapi.exe 多會話光碟。 如果是，IMAPI.EXE 會自動進入多會話模式。 在建立多會話模式後使用 [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) 會導致 imapi.exe 回到單一會話模式。 這表示 [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) 燒錄需要空白光碟。 如果光碟處於多重會話模式，則相同的光碟必須在使用中的錄製器中，否則將會傳回 IMAPI.EXE \_ E \_ WRONGDISC 的錯誤碼。

在 Joliet 格式中選取錄製器，會讓 IMAPI.EXE 從目前安裝的光碟讀取資訊。如果光碟是另一個會話具有空間的先前 IMAPI.EXE Joliet 光碟，IMAPI.EXE 會自動將自己設定為多會話模式。 呼叫 [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc)時，此光碟必須存在於使用中的錄製器中。

關閉光碟上的第一個會話需要 21 MB。 每個額外的會話都需要 11 MB 來關閉。

 

 




