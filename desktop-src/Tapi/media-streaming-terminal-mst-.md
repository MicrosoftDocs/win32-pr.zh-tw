---
description: 媒體串流終端 (MST) 是根據使用 DirectShow 篩選器的動態終端機。 使用 TAPI 3 MSP 基類撰寫的 MSP 會併入 MST，但 MSP 作者可以選擇在不使用基類的情況下加以執行。
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: '媒體串流終端 (MST) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945652"
---
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="a68a5-104">媒體串流終端 (MST) </span><span class="sxs-lookup"><span data-stu-id="a68a5-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="a68a5-105">媒體串流終端 (MST) 是根據使用 DirectShow 篩選器的動態終端機。</span><span class="sxs-lookup"><span data-stu-id="a68a5-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="a68a5-106">使用 [TAPI 3 MSP 基類](tapi-3-msp-base-classes.md) 撰寫的 msp 會併入 MST，但 msp 作者可以選擇在不使用基類的情況下加以執行。</span><span class="sxs-lookup"><span data-stu-id="a68a5-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="a68a5-107">若要叫用 MST 建立，應用程式會呼叫 [**ITTerminalSupport：： CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) ，並將 *PTERMINALCLASS* 設定為 CLSID \_ MediaStreamTerminal。</span><span class="sxs-lookup"><span data-stu-id="a68a5-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="a68a5-108">然後， [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) 和 [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) 介面會在終端機上公開，讓應用程式能夠調整串流效能。</span><span class="sxs-lookup"><span data-stu-id="a68a5-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="a68a5-109">這些介面是在 Tapi3 中宣告。</span><span class="sxs-lookup"><span data-stu-id="a68a5-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="a68a5-110">必須熟悉 DirectShow 篩選器和篩選圖表管理，才能實現和使用 MST。</span><span class="sxs-lookup"><span data-stu-id="a68a5-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="a68a5-111">請參閱平臺軟體發展工具組 (SDK) 的 [圖形和多媒體服務] 節點下的 DirectShow 材料。</span><span class="sxs-lookup"><span data-stu-id="a68a5-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="a68a5-112">多媒體串流參考將特別適用于 MSP 作者。</span><span class="sxs-lookup"><span data-stu-id="a68a5-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
