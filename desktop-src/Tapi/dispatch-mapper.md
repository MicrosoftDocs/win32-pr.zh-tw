---
description: 分派對應程式是使用 COM CoCreateInstance 建立的，並公開一個介面 ITDispatchMapper。
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: 分派對應程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998105"
---
# <a name="dispatch-mapper"></a>分派對應程式

分派對應程式是使用 COM **CoCreateInstance** 建立的，並公開一個介面 [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)。 這個介面可讓應用程式在指定某個介面的分派指標和另一個介面的 GUID 時，取得物件上另一個介面的分派指標。 此介面是提供來協助程式設計人員使用腳本應用程式，這些應用程式不會提供立即輪詢物件上介面的方法。

分派對應程式會使用物件的 **IObjectSafety** 介面，以確定物件在要求的介面上是安全的，以進行腳本處理。 如果物件不會執行 **IObjectSafety**，或此特定介面上的物件不安全，則呼叫會失敗。

 

 



