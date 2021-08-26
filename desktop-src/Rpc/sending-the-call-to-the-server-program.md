---
title: 傳送呼叫給伺服器程式
description: 一旦用戶端的 RPC 執行時間已連接到伺服器端點，它就會 marshalls 引數，並將其傳送至伺服器。
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- 遠端程序呼叫 RPC、工作、將呼叫傳送至伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a02d4fc1d69ba45cc6de3d43fba62724de1277471992790e3098225f579d305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017908"
---
# <a name="sending-the-call-to-the-server-program"></a>傳送呼叫給伺服器程式

一旦用戶端的 RPC 執行時間已連接到伺服器端點，它就會 marshalls 引數，並將其傳送至伺服器。 伺服器 RPC 執行時間會將已封送處理的引數提供給 unmarshalls 它們的存根，然後將它們傳遞給伺服器常式。 當伺服器常式傳回時，存根會挑選 \[ out \] 和 \[ in、out \] 參數和傳回值，marshalls 它們，然後將封送處理的資料傳送到伺服器 RPC 執行時間。 RPC 執行時間會將資料傳送回用戶端，其中用戶端 RPC 執行時間會將這些資料交給 unmarshalls 它們的用戶端存根，並傳回給呼叫者。

 

 




