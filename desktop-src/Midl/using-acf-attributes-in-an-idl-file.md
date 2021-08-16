---
title: 在 IDL 檔案中使用 ACF 屬性
description: 您可以使用/app \_ CONFIG MIDL 編譯器選項，在 IDL 檔案中指定系結控制碼屬性，而不是在個別的 ACF 檔中。
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- 在 IDL 中使用 ACF ACF MIDL、屬性
- IDL MIDL，使用 ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105518"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>在 IDL 檔案中使用 ACF 屬性

您可以使用/[**app \_ config**](-app-config.md) MIDL 編譯器選項，在 IDL 檔案中指定系結控制碼屬性，而不是在個別的 ACF 檔案中。 具體而言，您可以將 [**自動 \_ 控制碼**](auto-handle.md)、 [**隱含 \_ 控制碼**](implicit-handle.md)和 [**明確的 \_ 控制碼**](explicit-handle.md) 屬性套用至 IDL 檔案中 RPC 介面的標頭。 如果您的 RPC 應用程式不需要其他 ACF 屬性，而且您不需要嚴格的憑證-DCE 相容性，請考慮使用此選項。

 

 




