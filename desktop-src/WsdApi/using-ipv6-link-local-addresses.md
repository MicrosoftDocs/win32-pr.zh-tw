---
description: IPv6 連結-SOAP 訊息中的本機定址提供了獨特的挑戰，因為 IPv6 連結-本機位址需要範圍識別碼才有意義，但是範圍識別碼只有本機電腦的意義。
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: 使用 IPv6 連結-本機位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c1719e4e6d374e7afd859b80cd1bc14c4c841cb7dceee149f14d0acb777f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897158"
---
# <a name="using-ipv6-link-local-addresses"></a>使用 IPv6 連結-本機位址

IPv6 連結-SOAP 訊息中的本機定址提供了獨特的挑戰，因為 IPv6 連結-本機位址需要範圍識別碼才有意義，但是範圍識別碼只有本機電腦的意義。 在 SOAP 訊息中傳送 IPv6 連結-本機位址之前，所有用戶端和裝置的執行都必須先移除範圍識別碼。 此外，當訊息中收到 IPv6 連結-本機位址時，收到訊息的介面必須是已知的，如此才能重建具有範圍識別碼的完整連結本機位址。

 

 



