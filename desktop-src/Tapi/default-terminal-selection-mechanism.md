---
description: Multitrack 終端機的概念讓 TAPI 更適合用來提供簡化的方法，讓您選取串流或串流上的終端機。 預設終端機選取機制的設計目的是要解決此情況。
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: 預設終端機選取機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847859"
---
# <a name="default-terminal-selection-mechanism"></a>預設終端機選取機制

[Multitrack 終端](multitrack-terminals.md)機的概念讓 TAPI 更適合用來提供簡化的方法，讓您選取串流或串流上的終端機。 預設終端機選取機制的設計目的是要解決此情況。

## <a name="selecting-a-terminal-on-a-call"></a>選取來電上的終端機

預設的終端機選取功能是透過在通話時選取終端機的功能所提供。

[呼叫物件](call-object.md)會公開新的介面 [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)。 介面會公開與 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)相同的方法，加上三個新的方法： [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal)、 [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)和 [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall)。

**ITBasicCallControl2：： RequestTerminal** 會建立終端機，並提供終端機類別、方向和媒體類型。 它會查看支援的靜態和動態終端機清單，以尋找並建立要求的終端機。

[**ITBasicCallControl2：： SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) 會選取終端 (或者在 multitrack 終端機、列舉、視需要建立，然後選取資料流程 (的追蹤終端機) ，或可在呼叫上取得的資料流程) 。

[**ITBasicCallControl2：： SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)的檔將說明將呼叫串流用於比對終端機 (或追蹤可在終端機) 上使用的演算法。

呼叫 [**ITBasicCallControl2：： UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) 會導致終端機 (單一追蹤或 multitrack) 從呼叫中取消選取。 如需詳細資訊，請參閱方法的檔。

## <a name="selecting-a-terminal-on-itstream"></a>選取 ITStream 上的終端機

藉由呼叫 [**ITStream：：) SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)選取 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (上的單一追蹤終端機，會選取資料流程上的終端機。 這是一般的 TAPI 3 終端機選擇程式。

只可在資料流程上選取單一追蹤終端機。 選取串流上的 multitrack 終端機將會失敗，因為資料流程將無法辨識媒體類型和方向。

 

 
