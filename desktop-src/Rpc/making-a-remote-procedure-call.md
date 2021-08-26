---
title: 進行遠端程序呼叫
description: 一旦使用明確系結控制碼的分散式應用程式的用戶端程式具有系結控制碼，就可以執行遠端程式。
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- 遠端程序呼叫 RPC、工作、進行呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8218fd99e11c65f15dbbe7a56c2ece1b93720839498352d610312a0f66f95bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020078"
---
# <a name="making-a-remote-procedure-call"></a>進行遠端程序呼叫

一旦使用明確系結控制碼的分散式應用程式的用戶端程式具有系結控制碼，就可以執行遠端程式。

Microsoft RPC 也提供自訂系結控制碼、隱含的系結控制碼，以及自動系結控制碼。 這些系結處理可提供用戶端和伺服器程式不同層級的控制，以控制執行遠端程式的過程。 如需不同的控制碼類型以及它們所提供之彈性的詳細資訊，請參閱系結 [和控點](binding-and-handles.md)。

若要從遠端執行程序呼叫，請以呼叫任何 C 函數的相同方式來呼叫用戶端存根函式。

 

 




