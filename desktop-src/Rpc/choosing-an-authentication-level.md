---
title: 選擇驗證層級
description: 選擇驗證等級時，請使用下列指導方針。
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac5610efad7ae1149d3c6555e2a005e3870a4f0e55983a17457bfa130561f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073458"
---
# <a name="choosing-an-authentication-level"></a>選擇驗證層級

選擇驗證等級時，請使用下列指導方針。 如果所傳送的資料是否可以被攔截和修改，且接收的資料可以被攔截或修改，請使用 RPC \_ C \_ 驗證 \_ LEVEL \_ NONE （預設值）。 如果不應該修改資料，而且不會傳送或接收私人資料，請使用 RPC \_ C \_ 驗證 \_ 層級 \_ 的 PKT \_ 完整性。 在所有其他情況下，請使用 RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權。

請勿使用 RPC \_ c \_ 驗證 \_ 層級 \_ 的預設值、rpc \_ c \_ 驗證 \_ 層級 \_ CONNECT、rpc \_ c \_ 驗證 \_ 層級 \_ 呼叫或 rpc \_ c \_ 驗證 \_ 層級 \_ PKT。 複雜的攻擊者可以中斷這些驗證層級，並使其失效。 其中每個層級都會讓攻擊者稍微難以攔截和修改資料，並進行模擬，但無法真正達成安全性。 由於攻擊者的複雜性層級很罕見，因此並非明智的選擇。

 

 




