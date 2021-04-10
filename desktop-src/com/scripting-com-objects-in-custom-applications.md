---
title: 在自訂應用程式中編寫 COM 物件的腳本
description: 在自訂應用程式中編寫 COM 物件的腳本
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183394"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="b4a2f-103">在自訂應用程式中編寫 COM 物件的腳本</span><span class="sxs-lookup"><span data-stu-id="b4a2f-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="b4a2f-104">Microsoft 提供數個用於編寫 COM 物件腳本的環境： Active Server Pages、Windows Script Host 等等。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="b4a2f-105">獨立軟體廠商 (Isv) 也可以授權 Microsoft 腳本引擎在其應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="b4a2f-106">例如，建立字組處理器的 ISV 可能會想要在應用程式中加入宏語言，讓使用者可以將簡單的工作自動化。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="b4a2f-107">藉由授權腳本引擎，ISV 可以使用 VBScript 或 JScript 之類的語言作為應用程式的宏語言。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="b4a2f-108">除了授權 VBScript 和 JScript 腳本引擎之外，Isv 還可以撰寫自己的 ActiveX 腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="b4a2f-109">然後，這些腳本引擎可以插入任何支援 ActiveX 腳本引擎標準的主機環境中。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="b4a2f-110">例如，ISV 可能會撰寫 PerlScript 腳本引擎，並將它安裝在 ASP 伺服器上，因此可讓 ASP 伺服器處理 PerlScript 腳本。</span><span class="sxs-lookup"><span data-stu-id="b4a2f-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4a2f-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4a2f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4a2f-112">使用 COM 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="b4a2f-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




