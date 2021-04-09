---
title: 在 IDL 檔案中使用 ACF 屬性
description: 您可以使用/app \_ CONFIG MIDL 編譯器選項，在 IDL 檔案中指定系結控制碼屬性，而不是在個別的 ACF 檔中。
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- 在 IDL 中使用 ACF ACF MIDL、屬性
- IDL MIDL，使用 ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dde95201bc2c729ac126b35e04919fd196cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672743"
---
# <a name="using-acf-attributes-in-an-idl-file"></a><span data-ttu-id="b54c4-105">在 IDL 檔案中使用 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="b54c4-105">Using ACF Attributes in an IDL File</span></span>

<span data-ttu-id="b54c4-106">您可以使用/[**app \_ config**](-app-config.md) MIDL 編譯器選項，在 IDL 檔案中指定系結控制碼屬性，而不是在個別的 ACF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b54c4-106">You can use the /[**app\_config**](-app-config.md) MIDL compiler option to specify binding handle attributes in the IDL file rather than in a separate ACF file.</span></span> <span data-ttu-id="b54c4-107">具體而言，您可以將 [**自動 \_ 控制碼**](auto-handle.md)、 [**隱含 \_ 控制碼**](implicit-handle.md)和 [**明確的 \_ 控制碼**](explicit-handle.md) 屬性套用至 IDL 檔案中 RPC 介面的標頭。</span><span class="sxs-lookup"><span data-stu-id="b54c4-107">Specifically, you can apply the [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), and [**explicit\_handle**](explicit-handle.md) attributes to the header of an RPC interface in an IDL file.</span></span> <span data-ttu-id="b54c4-108">如果您的 RPC 應用程式不需要其他 ACF 屬性，而且您不需要嚴格的憑證-DCE 相容性，請考慮使用此選項。</span><span class="sxs-lookup"><span data-stu-id="b54c4-108">Consider using this option if your RPC application does not require other ACF attributes, and if you do not require strict OSF-DCE compatibility.</span></span>

 

 




