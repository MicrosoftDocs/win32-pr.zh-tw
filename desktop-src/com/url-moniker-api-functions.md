---
title: URL 標記函數
description: URL 標記函數
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db726d8ce6a101b0b97fbe2128e074ee5e892e3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842784"
---
# <a name="url-moniker-functions"></a>URL 標記函數

URL 標記函式會讓開發人員免于建立、管理及使用 URL 標記的複雜性。 這些函數如下所示：

-   [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

您熟悉這些功能的方式如下：

-   如果您在獨立應用程式中使用 URL 的名字標記，請熟悉 [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) 和 [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) 。 如果您要撰寫 ActiveX 控制項，您應該使用 [**IBindHost：： CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) 而不是 **CreateURLMoniker**。
-   如果您要使用 URL 標記來執行任何 MIME 協商，請熟悉 [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))、 [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)、 [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))和 [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) 。
-   只有當您有大量的 URL 名字和 COM 的體驗時，才熟悉 [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))、 [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))、 [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))和 [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[URL 的名字](url-monikers.md)
</dt> </dl>

 

 