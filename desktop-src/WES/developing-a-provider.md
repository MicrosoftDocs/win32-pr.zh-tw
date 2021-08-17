---
title: 開發提供者
description: 若要寫入您在資訊清單中定義的事件，您可以使用事件追蹤 (ETW) API 中所含的函式。 如需撰寫提供者的詳細資訊，請參閱提供事件。
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937183"
---
# <a name="developing-a-provider"></a>開發提供者

若要寫入您在資訊清單中定義的事件，您可以使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) API 中所含的函式。 如需撰寫提供者的詳細資訊，請參閱 [提供事件](/windows/desktop/ETW/providing-events)。

撰寫提供者之後，請使用 WevtUtil.exe 工具來註冊提供者和架構。 如需使用 WevtUtil 的詳細資訊，請參閱[Windows 事件記錄工具](windows-event-log-tools.md)。 以下顯示如何使用 WevtUtil 來註冊提供者和移除註冊。


```cmd
wevtutil im provider.man

wevtutil um provider.man
```