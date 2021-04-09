---
description: IPv6 連結-SOAP 訊息中的本機定址提供了獨特的挑戰，因為 IPv6 連結-本機位址需要範圍識別碼才有意義，但是範圍識別碼只有本機電腦的意義。
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: 使用 IPv6 連結-本機位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114273"
---
# <a name="using-ipv6-link-local-addresses"></a>使用 IPv6 連結-本機位址

IPv6 連結-SOAP 訊息中的本機定址提供了獨特的挑戰，因為 IPv6 連結-本機位址需要範圍識別碼才有意義，但是範圍識別碼只有本機電腦的意義。 在 SOAP 訊息中傳送 IPv6 連結-本機位址之前，所有用戶端和裝置的執行都必須先移除範圍識別碼。 此外，當訊息中收到 IPv6 連結-本機位址時，收到訊息的介面必須是已知的，如此才能重建具有範圍識別碼的完整連結本機位址。

 

 



