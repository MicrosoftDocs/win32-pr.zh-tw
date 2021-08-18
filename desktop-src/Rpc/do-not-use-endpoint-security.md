---
title: 請勿使用端點安全性
description: 端點安全性是一種安全性模型，在使用 RPC 函式的 RpcServerUseProtseq \ 群組建立端點時，會提供安全描述項。
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d302ec0d331eaadb3291e36b30084264b4a6331745110fc642dd2ede02c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930695"
---
# <a name="do-not-use-endpoint-security"></a>請勿使用端點安全性

端點安全性是一種安全性模型，在使用 RPC 函式的 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)群組建立端點時，會提供安全描述項 \* 。 請勿使用此安全性模型。 請勿將安全描述項提供給這些函式。 最棒的是，此方法會浪費 CPU 資源。 最糟的是，在許多環境中，您可以規避安全描述項，因為在相同的進程區段中執行的 [其他 RPC 端點](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) 」舉例說明。

端點安全性僅為了回溯相容性而存在。

 

 




