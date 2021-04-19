---
title: XML 語言支援
description: 本節說明 WWS 中的 XML 語言支援層級。
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- 適用于 Windows 的 XML 語言支援 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106967934"
---
# <a name="xml-language-support"></a><span data-ttu-id="83631-106">XML 語言支援</span><span class="sxs-lookup"><span data-stu-id="83631-106">XML Language Support</span></span>

<span data-ttu-id="83631-107">本節說明 WWS 中的 XML 語言支援層級。</span><span class="sxs-lookup"><span data-stu-id="83631-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="83631-108">請參閱 DownlevelLCIDToLocaleName 在 Windows Vista 之前的 Windows 版本上的函式，若要在 LCID 和 xml： lang 值之間轉換，請參閱 < a0/LCIDToLocalName < a1/&gt;。</span><span class="sxs-lookup"><span data-stu-id="83631-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="83631-109">讀取時，可能會使用 [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) 來探索範圍中 "xml： lang" 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="83631-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="83631-110">寫入時， [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) 可用來寫入 "xml： lang" 屬性。</span><span class="sxs-lookup"><span data-stu-id="83631-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




