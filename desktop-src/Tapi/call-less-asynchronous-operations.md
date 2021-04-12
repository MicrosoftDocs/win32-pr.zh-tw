---
description: 有五個與任何特定呼叫無關的非同步作業。
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: 不呼叫的非同步作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319255"
---
# <a name="call-less-asynchronous-operations"></a>不呼叫的非同步作業

有五個與任何特定呼叫無關的非同步作業。 TAPI 2.x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)、 [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)、 [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward)、 [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)和 [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) 函數會起始這些作業。 如果應用程式起始其中一個非同步作業，並呼叫 [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)，服務提供者可能不會收到應用程式已放棄函數的指示。 如果應用程式不是唯一讓該行開啟的應用程式，就會發生這種情況。 如果應用程式使用其中一個暫止的作業來呼叫 **lineClose** ，而且它是唯一具有該行控制碼的應用程式，則 TAPI 會呼叫 [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) 函式，而服務提供者應終止非同步作業，並針對每個這類未完成的作業呼叫 [*完成 \_ 程式回檔*](/windows/win32/api/tspi/nc-tspi-async_completion) 函式（LINEERR \_ OPERATIONFAILED 錯誤值）。

 

 
