---
description: 若要建立自訂擴充功能或編碼複雜的延伸模組，您可以撰寫自己的延伸模組處理常式來匯出自訂介面。
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: 撰寫自訂延伸模組處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987736"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="c9645-103">撰寫自訂延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="c9645-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="c9645-104">若要建立自訂擴充功能或編碼複雜的延伸模組，您可以撰寫自己的延伸模組處理常式來匯出自訂介面。</span><span class="sxs-lookup"><span data-stu-id="c9645-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="c9645-105">Microsoft 憑證服務隨附下列介面，可用來編碼各種類型的延伸資料： [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)、 [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)、 [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo)、 [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)、 [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)和 [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray)。</span><span class="sxs-lookup"><span data-stu-id="c9645-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="c9645-106">這些介面包含在 Certenc.dll 中。</span><span class="sxs-lookup"><span data-stu-id="c9645-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="c9645-107">此外，這些介面的類型資訊包含在 Certencl.dll 中，其中包含在平臺軟體發展工具組 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="c9645-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="c9645-108">如需擴充處理常式的詳細資訊，請參閱 [擴充處理常式](extension-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="c9645-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



